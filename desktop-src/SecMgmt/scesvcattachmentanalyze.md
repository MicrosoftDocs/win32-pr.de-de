---
description: Die scesvasetachmentanalysis-Funktion wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System analysiert wird.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: Scesvcalltachmentanalysis-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750873"
---
# <a name="scesvcattachmentanalyze-callback-function"></a>Scesvcalltachmentanalysis-Rückruffunktion

Die **scesvasetachmentanalysis** -Funktion wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System analysiert wird.

## <a name="syntax"></a>Syntax


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pscecbinfo* \[ in\]
</dt> <dd>

Zeiger auf eine [**scesvc \_ - \_ Rückruf**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Informationsstruktur, die ein undurchsichtiges Daten Bank Handle und Rückruf Funktionszeiger auf Abfrage-, festgelegte und kostenlose Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird "scestatus Success" zurückgegeben \_ . Andernfalls wird ein Fehlercode zurückgegeben. Weitere Informationen zu den Sicherheits Konfigurations-Fehlercodes finden Sie unter [Anhang Return Values](management-return-values.md).

## <a name="remarks"></a>Bemerkungen

Die **scesvtortachmentanalysis** -Funktion muss folgende Aktionen ausführen:

-   Direkte Abfrage von Konfigurationsinformationen aus dem Dienst.
-   Rufen Sie die Rückruffunktion auf, auf die vom **pfqueryinfo** -Member der [**scesvc- \_ Rückruf \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Informationsstruktur (pscecbinfo->pfqueryinfo) verwiesen wird, um Informationen aus der Sicherheitsdatenbank abzurufen.
-   Berechnen Sie die Unterschiede zwischen den Informationen auf der Grundlage von Typ und Syntax.
-   Rufen Sie die Rückruffunktion auf, auf die vom **pfset** -Member der [**scesvc- \_ Rückruf \_ Informations**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) Struktur (pscecbinfo->pfabtinfo) verwiesen wird, um die Sicherheitsdatenbank mit den abgerufenen Dienst Informationen zu aktualisieren, die sich unterscheiden.

Weitere Informationen finden Sie unter [Implementieren von scesvsintachmentanalysis](implementing-scesvcattachmentanalyze.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Implementieren von scesvpetachmentanalysis](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**scesvc- \_ Rückruf \_ Informationen**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**Scesvalisitachmentconfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




