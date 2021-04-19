---
description: Im folgenden finden Sie eine Beispiel Nachrichtendatei, die verwendet werden kann, um eine reine Ressourcen-DLL zu erstellen, die mit dem Dienst Beispiel beim Schreiben von Ereignissen in das Ereignisprotokoll verwendet werden kann.
ms.assetid: d0d46041-5608-4abf-b833-7aae1744ef60
title: Sample.mc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b34c87fad27b08671de57d7e329073df5a48579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352323"
---
# <a name="samplemc"></a>Sample.mc

Im folgenden finden Sie eine Beispiel Nachrichtendatei, die verwendet werden kann, um eine reine Ressourcen-DLL zu erstellen, die mit dem Dienst Beispiel beim Schreiben von Ereignissen in das Ereignisprotokoll verwendet werden kann.

Führen Sie die folgenden Schritte aus, um die dll zu erstellen:

1.  **MC-U Sample.MC**
2.  **RC-r-Beispiel. RC**
3.  **Link-dll-NOENTRY -out:sample.dll Sample. res**

``` syntax
MessageIdTypedef=DWORD

SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
    Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
    Warning=0x2:STATUS_SEVERITY_WARNING
    Error=0x3:STATUS_SEVERITY_ERROR
    )


FacilityNames=(System=0x0:FACILITY_SYSTEM
    Runtime=0x2:FACILITY_RUNTIME
    Stubs=0x3:FACILITY_STUBS
    Io=0x4:FACILITY_IO_ERROR_CODE
)

LanguageNames=(English=0x409:MSG00409)

; // The following are message definitions.

MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=SVC_ERROR
Language=English
An error has occurred (%2).
.

; // A message file must end with a period on its own line
; // followed by a blank line.
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Complete Service-Beispiel](the-complete-service-sample.md)
</dt> </dl>

 

 



