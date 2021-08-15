---
description: Eine anwendungsdefinierte Funktion, die Rückrufzugriffssteuerungseinträge (Access Control Entries, ACEs) während einer Zugriffsüberprüfung verarbeitet.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Rückruffunktion "AccessCheckCallback" inHz
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5079b740d268174715b6c944787bb687cd9b8b1ecb12a27c04eeb26c79811034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784156"
---
# <a name="authzaccesscheckcallback-callback-function"></a>Rückruffunktion "AccessCheckCallback" inHz

Die **Funktion "SollhzAccessCheckCallback"** ist eine anwendungsdefinierte Funktion, die Rückruf-Zugriffssteuerungseinträge (Callback [*Access Control Entries,*](/windows/desktop/SecGloss/a-gly) ACEs) während einer Zugriffsüberprüfung verarbeitet. **HzAccessCheckCallback** ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen. Die Anwendung registriert diesen Rückruf, indem [**sie BlendhzInitializeResourceManager aufruft.**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hAuthzClientContext* \[ In\]
</dt> <dd>

Ein Handle für einen Clientkontext.

</dd> <dt>

*pAce* \[ In\]
</dt> <dd>

Ein Zeiger auf den ACE, der ausgewertet werden soll, um ihn in den Aufruf der [**Funktion "SollhzAccessCheck" einschlussen zu**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) können.

</dd> <dt>

*pArgs* \[ in, optional\]
</dt> <dd>

Daten, die im *DynamicGroupArgs-Parameter* des Aufrufs von [**"MusshzAccessCheck"**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) oder [**"AghzCachedAccessCheck" übergeben werden.**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)

</dd> <dt>

*pbAceApplicable* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine boolesche Variable, die die Ergebnisse der Auswertung der von der Anwendung definierten Logik empfängt.

Die Ergebnisse sind **TRUE,** wenn die Logik feststellt, dass der ACE anwendbar ist, und wird in den Aufruf von [**BishzAccessCheck eingeschlossen.**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) Andernfalls sind die Ergebnisse **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion **TRUE zurück.**

Wenn die Funktion die Auswertung nicht ausführen kann, gibt sie **FALSE zurück.** Verwenden [**Sie SetLastError,**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) um einen Fehler an die Zugriffsüberprüfungsfunktion zurück zu geben.

## <a name="remarks"></a>Hinweise

Sicherheitsattributvariablen müssen im Clientkontext vorhanden sein, wenn in einem bedingten Ausdruck darauf verwiesen wird. Andernfalls wird der Begriff des bedingten Ausdrucks, auf den sie verweisen, als unbekannt ausgewertet.

Weitere Informationen finden Sie unter [How AccessCheck Works (Funktionsweise von AccessCheck)](how-dacls-control-access-to-an-object.md) und [Centralized Authorization Policy overviews](centralized-authorization-policy.md) (Übersicht über zentralisierte Autorisierungsrichtlinien).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                   |
| Verteilbare Komponente<br/>          | Windows Server 2003 Administration Tools Pack auf Windows XP<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Grundlegende Access Control Funktionen](authorization-functions.md)
</dt> <dt>

[Zentralisierte Autorisierungsrichtlinie](centralized-authorization-policy.md)
</dt> <dt>

[Funktionsweise von AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**HzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[**CodhzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**QshzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**QshzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

