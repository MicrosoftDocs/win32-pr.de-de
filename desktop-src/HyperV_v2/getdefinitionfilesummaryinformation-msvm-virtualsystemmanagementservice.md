---
description: Gibt Zusammenfassungsinformationen für virtuelle Computer für die angegebenen VM-Definitionsdateien zurück.
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
ms.openlocfilehash: 7c6d3da6ef920488edb7fde723880b9f53768cfd246e91d287390bb6fb02fb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995297"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>GetDefinitionFileSummaryInformation-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Gibt Zusammenfassungsinformationen für virtuelle Computer für die angegebenen VM-Definitionsdateien zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DefinitionFiles* \[ In\]
</dt> <dd>

Ein Array von Pfaden zu XML-Konfigurationsdateien, für die Zusammenfassungsinformationen zurückgegeben werden sollen.

</dd> <dt>

*SummaryInformation* \[ out\]
</dt> <dd>

Ein Array von [**Msvm \_ SummaryInformationBase-Instanzen,**](msvm-summaryinformation.md) das die angeforderten Informationen für die virtuellen Computer und/oder Momentaufnahmen enthält, die im *DefinitionFiles-Array* angegeben sind. Nur die Eigenschaften **Name,** **ElementName,** **CreationTime** und **Notes** werden zurückgegeben. Alle anderen Eigenschaften sind **NULL.**

> [!Note]  

 

Vor Windows 10 Version 1703 war der Datentyp [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




