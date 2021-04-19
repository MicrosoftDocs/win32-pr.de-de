---
description: Mit der "ankündigen"-Methode des Installerobjekts wird ein Installationspaket angekündigt.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Installer:: ankündigen-Product-Methode'
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
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369715"
---
# <a name="installeradvertiseproduct-method"></a>Installer:: ankündigen-Product-Methode

Mit der "ankündigen" **-Methode des** [**Installerobjekts**](installer-object.md) wird ein Installationspaket angekündigt.

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

Der vollständige Pfad zum Windows Installer Paket (. msi), das angekündigt werden soll.

</dd> <dt>

*context* 
</dt> <dd>

Der Kontext der Ankündigung. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <dt>**msiankündigen-productmachine**</dt> <dt>0</dt> </dl> | Kündigt die Anwendung für eine [Installation im Installations Kontext](installation-context.md)pro Computer an. Dadurch wird das Paket für die Installation durch alle Benutzer des Computers zur Verfügung gestellt.<br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <dt>**msiankündigen**</dt> <dt>1</dt> </dl>             | Kündigt die Anwendung für eine Installation im [Installations Kontext](installation-context.md)pro Benutzer an.<br/>                                                                                   |



 

</dd> <dt>

*Kranz* 
</dt> <dd>

Die Liste der Transformationen, die auf das Produkt angewendet werden sollen. Transformationen in der Liste werden durch Semikolons getrennt. Dieser Parameter ist optional.

</dd> <dt>

*language* 
</dt> <dd>

Die Sprache des zu verwendenden Installationspakets. Dieser Parameter ist optional.

</dd> <dt>

*options* 
</dt> <dd>

Die Ankündigungs Optionen. Dieser Parameter ist optional. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiankündigen-Standard**</dt> Wert <dt>0</dt> </dl>                             | Standard Ankündigung<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiwerbesesinglabstance**</dt> <dt>1</dt> </dl> | Gibt eine neue Instanz des Produkts an. Erfordert, dass die erste Transformation in der Transformations Liste des *Transformationen* -Parameters die instanztransformation ist, mit der der Produktcode geändert wird. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **Methode "** ankündigen" verwendet die [**msiankündigen-productex**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) -Funktion.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der-Methode von " **Werbung** " veranschaulicht.


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
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installationsprogramm**](installer-object.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




