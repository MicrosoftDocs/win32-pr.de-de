---
description: Gibt Informationen zur Zusammenfassung der virtuellen Computer für die angegebenen Definitions Dateien der virtuellen Maschine zurück.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: GetDefinitionFileSummaryInformation-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357370"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>GetDefinitionFileSummaryInformation-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Gibt Informationen zur Zusammenfassung der virtuellen Computer für die angegebenen Definitions Dateien der virtuellen Maschine zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DefinitionFiles* \[ in\]
</dt> <dd>

Ein Array von Pfaden zu XML-Konfigurationsdateien, für die Zusammenfassungs Informationen zurückgegeben werden sollen.

</dd> <dt>

*SummaryInformation* \[ vorgenommen\]
</dt> <dd>

Ein Array von [**MSVM- \_ summaryinformationbase**](msvm-summaryinformation.md) -Instanzen, die die angeforderten Informationen für die virtuellen Computer und/oder Momentaufnahmen enthalten, die im *DefinitionFiles* -Array angegeben sind. Nur die Eigenschaften **Name**, **ElementName**, **kreationtime** und **Notes** werden zurückgegeben, alle anderen Eigenschaften sind **null**.

> [!Note]  

 

Vor Windows 10, Version 1703, war Datentyp [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




