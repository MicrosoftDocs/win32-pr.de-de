---
description: Die PatchProperty-Eigenschaft ruft Informationen zu einem bestimmten Patch ab, der auf eine bestimmte Instanz des Produkts angewendet wird. Diese Eigenschaft ruft MsiGetPatchInfoEx auf.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Patch.PatchProperty-Methode
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
ms.openlocfilehash: a18fcd835624f102f81e6159d32d8dbb40eb07f016d7b00c681248eac128e642
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381330"
---
# <a name="patchpatchproperty-method"></a>Patch.PatchProperty-Methode

Die **PatchProperty-Eigenschaft** ruft Informationen zu einem bestimmten Patch ab, der auf eine bestimmte Instanz des Produkts angewendet wird. Diese Eigenschaft ruft [**MsiGetPatchInfoEx auf.**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)

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

Der *szProperty-Parameter* kann einer der folgenden Werte sein.



| Name          | Bedeutung                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocalPackage  | Dient zum Herunterladen der zwischengespeicherten Patchdatei, die vom Produkt verwendet wird.                                                                                                                                                                                                                                                                               |
| Transformationen    | Hier finden Sie die Patchtransformationen, die bei der letzten Patchinstallation auf das Produkt angewendet wurden. Dieser Wert ist möglicherweise nicht für benutzerspezifische, nicht verwaltete Anwendungen verfügbar, wenn der Benutzer nicht am Computer angemeldet ist.                                                                                                                     |
| InstallDate   | Gibt das Datum an, an dem der Patch auf das Produkt angewendet wurde.                                                                                                                                                                                                                                                                      |
| Deinstallationsfähig | Gibt "1" zurück, wenn der Patch so markiert ist, dass er aus dem Produkt deinstalliert werden kann. In diesem Fall kann das Installationsprogramm die Deinstallation weiterhin blockieren, wenn dieser Patch für einen anderen Patch erforderlich ist, der nicht deinstalliert werden kann.                                                                                                          |
| State         | Gibt "1" zurück, wenn dieser Patch derzeit auf das Produkt angewendet wird. Gibt "2" zurück, wenn dieser Patch durch einen anderen Patch ersetzt wurde. Gibt "4" zurück, wenn dieser Patch durch einen anderen Patch veraltet gemacht wurde. Diese Werte entsprechen den Konstanten, die vom *dwFilter-Parameter* von [**MsiEnumPatchesEx verwendet werden.**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) |
| DisplayName   | Hier erhalten Sie den registrierten Anzeigenamen für den Patch. Bei Patches, die nicht die DisplayName-Eigenschaft in der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) enthalten, ist der zurückgegebene Anzeigename eine leere Zeichenfolge ("").                                                                                                      |
| MoreInfoURL   | Hier erhalten Sie die url der registrierten Supportinformationen für den Patch. Bei Patches, die nicht die MoreInfoURL-Eigenschaft in der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) enthalten, ist die zurückgegebene URL für Unterstützungsinformationen eine leere Zeichenfolge ("").                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode kann ERROR UNKNOWN PATCH zurückgeben, wenn das Patch-Objekt mit einer leeren Zeichenfolge für \_ \_ *ProductCode initialisiert wird.* [](patch-object.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch ist als \_ 000C10A1-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




