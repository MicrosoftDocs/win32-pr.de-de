---
description: Die SceSvcAttachmentAnalyze-Funktion wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System analysiert wird.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: SceSvcAttachmentAnalyze-Rückruffunktion
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
ms.openlocfilehash: 9bb84cc6a8492c729926b644a246b8ee8a03e1de4c2eae6e3de1fd88c5ba339f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004918"
---
# <a name="scesvcattachmentanalyze-callback-function"></a>SceSvcAttachmentAnalyze-Rückruffunktion

Die **SceSvcAttachmentAnalyze-Funktion** wird von der Sicherheitskonfigurations-Engine aufgerufen, wenn das System analysiert wird.

## <a name="syntax"></a>Syntax


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSceCbInfo* \[ In\]
</dt> <dd>

Zeiger auf eine [**SCESVC \_ CALLBACK \_ INFO-Struktur,**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) die ein nicht transparentes Datenbankhandler und Rückruffunktionszeiger zum Abfragen, Festlegen und Freien von Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ist, wird SCESTATUS \_ SUCCESS zurückgegeben. Andernfalls wird ein Fehlercode zurückgegeben. Weitere Informationen zu den Sicherheitskonfigurationsfehlercodes finden Sie unter [Attachment Return Values](management-return-values.md).

## <a name="remarks"></a>Hinweise

Die **SceSvcAttachmentAnalyze-Funktion** muss folgende Aufgaben erfüllen:

-   Direktes Abfragen von Konfigurationsinformationen vom Dienst.
-   Rufen Sie die Rückruffunktion auf, auf die das **pfQueryInfo-Element** der [**SCESVC \_ CALLBACK \_ INFO-Struktur**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) verweist, um Informationen aus der Sicherheitsdatenbank abzurufen.
-   Berechnen Sie die Unterschiede zwischen den Informationen basierend auf Typ und Syntax.
-   Rufen Sie die Rückruffunktion auf, auf die das **pfSetInfo-Element** der [**SCESVC \_ CALLBACK \_ INFO-Struktur**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) verweist, um die Sicherheitsdatenbank mit den abgerufenen Dienstinformationen zu aktualisieren, die sich unterscheiden.

Weitere Informationen finden Sie unter [Implementieren von SceSvcAttachmentAnalyze.](implementing-scesvcattachmentanalyze.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Implementieren von SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**\_SCESVC-RÜCKRUFINFORMATIONEN \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




