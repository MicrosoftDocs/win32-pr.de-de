---
description: Das SummaryInfo-Objekt wird verwendet, um Dokumenteigenschaften aus dem Zusammenfassungsinformationsdatenstrom eines Speicherobjekts zu lesen, zu erstellen und zu aktualisieren.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: SummaryInfo-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3efdc009f40f0bce67559d185afb4cba1289c00fc1d7771a43d392601220dbae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039590"
---
# <a name="summaryinfo-object"></a>SummaryInfo-Objekt

Das **SummaryInfo-Objekt** wird verwendet, um Dokumenteigenschaften aus dem [Zusammenfassungsinformationsdatenstrom](summary-information-stream.md) eines Speicherobjekts zu lesen, zu erstellen und zu aktualisieren.

## <a name="members"></a>Member

Das **SummaryInfo-Objekt** weist diese Typen von Membern auf:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SummaryInfo-Objekt** verfügt über diese Methoden.



| Methode                                 | BESCHREIBUNG                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Speichern**](summaryinfo-persist.md) | Formatiert und schreibt die zuvor gespeicherten Eigenschaften in den [standardmäßigen Zusammenfassungsinformationsdatenstrom.](summary-information-stream.md)<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **SummaryInfo-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | BESCHREIBUNG                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Property-Eigenschaft (SummaryInfo-Objekt)**](summaryinfo-summaryinfo.md)<br/> | Ruft den Wert für die angegebene Eigenschaft im Zusammenfassungsinformationsdatenstrom ab oder legt den Wert fest.<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | Gibt die aktuelle Anzahl von Eigenschaftswerten im Zusammenfassungsinformationsobjekt an.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo ist als 000C109B-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SummaryInformation-Eigenschaft (Datenbankobjekt)**](database-summaryinformation.md)
</dt> <dt>

[**SummaryInformation-Eigenschaft (Installer-Objekt)**](installer-summaryinformation.md)
</dt> <dt>

[Windows Beispiele für Skripterstellung für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




