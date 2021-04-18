---
description: Die patchproperty-Eigenschaft ruft Informationen zu einem bestimmten Patch ab, der auf eine bestimmte Instanz des Produkts angewendet wird. Diese Eigenschaft ruft msigetpatchinfoex auf.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Patch. patchproperty-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372569"
---
# <a name="patchpatchproperty-method"></a>Patch. patchproperty-Methode

Die **patchproperty** -Eigenschaft ruft Informationen zu einem bestimmten Patch ab, der auf eine bestimmte Instanz des Produkts angewendet wird. Diese Eigenschaft ruft [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)auf.

## <a name="syntax"></a>Syntax


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szProperty* 
</dt> <dd>

Der *szProperty* -Parameter kann einen der folgenden Werte aufweisen.



| Name          | Bedeutung                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Localpackage  | Dient zum erhalten der vom Produkt verwendeten zwischengespeicherten Patchdatei.                                                                                                                                                                                                                                                                               |
| Transformationen    | Holen Sie sich den Satz von patchtransformationen, die bei der letzten Patchinstallation auf das Produkt angewendet wurden. Dieser Wert ist möglicherweise nicht für pro-Benutzer-nicht verwaltete Anwendungen verfügbar, wenn der Benutzer nicht am Computer angemeldet ist.                                                                                                                     |
| InstallDate   | Das Datum der Anwendung des Patches auf das Produkt erhalten.                                                                                                                                                                                                                                                                      |
| Deinstallierbaren | Gibt "1" zurück, wenn der Patch so gekennzeichnet ist, dass er vom Produkt deinstalliert werden kann. In diesem Fall kann das Installationsprogramm die Deinstallation weiterhin blockieren, wenn dieser Patch von einem anderen Patch benötigt wird, der nicht deinstalliert werden kann.                                                                                                          |
| State         | Gibt "1" zurück, wenn dieser Patch aktuell auf das Produkt angewendet wird. Gibt "2" zurück, wenn dieser Patch durch einen anderen Patch ersetzt wurde. Gibt "4" zurück, wenn dieser Patch von einem anderen Patch veraltet gemacht wurde. Diese Werte entsprechen den Konstanten, die vom *dwfilter* -Parameter von [**msienüberpatchesex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)verwendet werden. |
| DisplayName   | Hiermit wird der registrierte Anzeige Name für den Patch angezeigt. Bei Patches, die die DisplayName-Eigenschaft in der [MsiPatchMetadata](msipatchmetadata-table.md) -Tabelle nicht enthalten, ist der zurückgegebene Anzeige Name eine leere Zeichenfolge ("").                                                                                                      |
| MoreInfoUrl   | Die registrierte Support Informations-URL für den Patch erhalten. Bei Patches, die die MoreInfoUrl-Eigenschaft in der [MsiPatchMetadata](msipatchmetadata-table.md) -Tabelle nicht enthalten, ist die zurückgegebene URL der Unterstützungs Informationen eine leere Zeichenfolge ("").                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann den Fehler "Unbekannter Patch" zurückgeben \_ \_ , wenn das [**Patch**](patch-object.md) -Objekt mit einer leeren Zeichenfolge für " *ProductCode*" initialisiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**Msienum patchesex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**Msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




