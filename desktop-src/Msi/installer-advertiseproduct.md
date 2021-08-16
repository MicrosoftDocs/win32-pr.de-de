---
description: Die AdvertiseProduct-Methode des Installer-Objekts kündigt ein Installationspaket an.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: Installer::AdvertiseProduct-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a3792b279df9ac43fc09eaa02005cdaf3373e341bf2df40ce0a350d6c31bd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633289"
---
# <a name="installeradvertiseproduct-method"></a>Installer::AdvertiseProduct-Methode

Die **AdvertiseProduct-Methode** des [**Installer-Objekts**](installer-object.md) kündigt ein Installationspaket an.

## <a name="syntax"></a>Syntax


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*packagePath* 
</dt> <dd>

Der vollständige Pfad zum Windows Installer-Paket (.msi), das angekündigt werden soll.

</dd> <dt>

*context* 
</dt> <dd>

Der Kontext der Ankündigung. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt> </dl> | Kündigt die Anwendung für eine Installation im [Installationskontext](installation-context.md)pro Computer an. Dadurch wird das Paket für die Installation durch alle Benutzer des Computers verfügbar.<br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <dt>**msiAdvertiseProductUser**</dt> <dt>1</dt> </dl>             | Kündigt die Anwendung für eine Installation im [Benutzer-Installationskontext](installation-context.md)an.<br/>                                                                                   |



 

</dd> <dt>

*Verwandelt* 
</dt> <dd>

Die Liste der Transformationen, die auf das Produkt angewendet werden sollen. Transformationen in der Liste werden durch Semikolons getrennt. Dieser Parameter ist optional.

</dd> <dt>

*language* 
</dt> <dd>

Die Sprache des zu verwendenden Installationspakets. Dieser Parameter ist optional.

</dd> <dt>

*options* 
</dt> <dd>

Die Ankündigungsoptionen. Dieser Parameter ist optional. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | Standardankündigung<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | Kündigt eine neue Instanz des Produkts an. Erfordert, dass die erste Transformation in der *Transformationsliste des Transformationsparameters* die Instanztransformation ist, die den Produktcode ändert. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches.](installing-multiple-instances-of-products-and-patches.md)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **AdvertiseProduct-Methode** verwendet die [**MsiAdvertiseProductEx-Funktion.**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **AdvertiseProduct-Methode** veranschaulicht.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 4.5 auf Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Installer**](installer-object.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




