---
description: Das SummaryInfo-Objekt wird verwendet, um Dokumenteigenschaften aus dem Zusammenfassungs Informationsdaten Strom eines Speicher Objekts zu lesen, zu erstellen und zu aktualisieren.
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
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351366"
---
# <a name="summaryinfo-object"></a>SummaryInfo-Objekt

Das **SummaryInfo** -Objekt wird verwendet, um Dokumenteigenschaften aus dem [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) eines Speicher Objekts zu lesen, zu erstellen und zu aktualisieren.

## <a name="members"></a>Member

Das **SummaryInfo** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SummaryInfo** -Objekt verfügt über diese Methoden.



| Methode                                 | BESCHREIBUNG                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Speichern**](summaryinfo-persist.md) | Formatiert und schreibt die zuvor gespeicherten Eigenschaften in den [standardzusammenfassungs-Informationsdaten Strom](summary-information-stream.md).<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **SummaryInfo** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                             | BESCHREIBUNG                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Property-Eigenschaft (SummaryInfo-Objekt)**](summaryinfo-summaryinfo.md)<br/> | Ruft den Wert für die angegebene Eigenschaft im Zusammenfassungs Informationsdaten Strom ab oder legt diesen fest.<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | Gibt die aktuelle Anzahl der Eigenschaftswerte im Zusammenfassungs Informationsobjekt an.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ isummaryinfo ist definiert als 000c109b-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SummaryInformation (Eigenschaft) (Datenbankobjekt)**](database-summaryinformation.md)
</dt> <dt>

[**SummaryInformation-Eigenschaft (Installer-Objekt)**](installer-summaryinformation.md)
</dt> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




