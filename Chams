using System;
using UnityEngine;

// Token: 0x02000468 RID: 1128
public class Chams : global::UnityEngine.MonoBehaviour
{
	// Token: 0x06001A93 RID: 6803
	private void Start()
	{
	}

	// Token: 0x06001A94 RID: 6804
	public void Update()
	{
		this.CreateChamMaterial();
		this.DoHacks();
	}

	// Token: 0x06001A95 RID: 6805
	public static void chamsLoader()
	{
		global::Chams.load_object = new global::UnityEngine.GameObject("Chams");
		global::Chams.load_object.AddComponent<global::Chams>();
		global::UnityEngine.Object.DontDestroyOnLoad(global::Chams.load_object);
	}

	// Token: 0x06001A96 RID: 6806
	public void CreateChamMaterial()
	{
		if (global::Chams.ChamMaterial)
		{
			global::Chams.ChamMaterial = new global::UnityEngine.Material("Shader \"Custom/Cham\"{\tSubShader \t{\t\tPass \t\t{\t\t\tZTest Less\t\t\tZWrite On\t\t\tColor (1,0,0,1) \t\t}\t\tPass \t\t{\t\t\tZTest Greater\t\t\tZWrite Off\t\t\tColor (0,1,0,1)\t\t}\t}}");
			global::Chams.ChamMaterial.hideFlags = global::UnityEngine.HideFlags.HideAndDontSave;
			global::Chams.ChamMaterial.shader.hideFlags = global::UnityEngine.HideFlags.HideAndDontSave;
			global::Chams.ChamMats = new global::UnityEngine.Material[]
			{
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial,
				global::Chams.ChamMaterial
			};
		}
	}

	// Token: 0x06001A97 RID: 6807
	public void DoHacks()
	{
		if (global::Chams.Updateskins < global::UnityEngine.Time.time)
		{
			global::Chams.skins = (global::UnityEngine.Object.FindObjectsOfType(typeof(global::UnityEngine.SkinnedMeshRenderer)) as global::UnityEngine.SkinnedMeshRenderer[]);
			global::Chams.Updateskins = global::UnityEngine.Time.time + 1f;
		}
		if (global::Chams.Cham && global::Vars.skins != null)
		{
			foreach (global::UnityEngine.SkinnedMeshRenderer skinnedMeshRenderer in global::Chams.skins)
			{
				if (!global::UnityEngine.Camera.main || (skinnedMeshRenderer.transform.root.position - global::UnityEngine.Camera.main.transform.position).magnitude >= 3f)
				{
					skinnedMeshRenderer.materials = global::Chams.ChamMats;
				}
			}
		}
	}

	// Token: 0x06001A98 RID: 6808
	public Chams()
	{
	}

	// Token: 0x04001A03 RID: 6659
	public static global::UnityEngine.GameObject load_object;

	// Token: 0x04001A5A RID: 6746
	public static float Updateskins;

	// Token: 0x04001A5B RID: 6747
	public static global::UnityEngine.Material ChamMaterial;

	// Token: 0x04001A5C RID: 6748
	public static global::UnityEngine.Material[] ChamMats;

	// Token: 0x04001A5D RID: 6749
	public static global::UnityEngine.SkinnedMeshRenderer[] skins;

	// Token: 0x04001A69 RID: 6761
	public static bool Cham;
}
