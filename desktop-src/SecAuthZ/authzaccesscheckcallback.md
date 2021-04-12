---
description: Eine Anwendungs definierte Funktion, die Rückruf-Zugriffs Steuerungs Einträge (ACEs) während einer Zugriffs Überprüfung behandelt.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Authzaccesscheckcallback-Rückruffunktion
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
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218836"
---
# <a name="authzaccesscheckcallback-callback-function"></a>Authzaccesscheckcallback-Rückruffunktion

Die **authzaccesscheckcallback** -Funktion ist eine Anwendungs definierte Funktion, die Rückruf- [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) während einer Zugriffs Überprüfung verarbeitet. **Authzaccesscheckcallback** ist ein Platzhalter für den Namen der Anwendungs definierten Funktion. Die Anwendung registriert diesen Rückruf durch Aufrufen von [**authzinitializeresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).

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

" *hauthzclientcontext* \[ " in\]
</dt> <dd>

Ein Handle für einen Client Kontext.

</dd> <dt>

*Geschwindigkeit* \[ in\]
</dt> <dd>

Ein Zeiger auf den ACE, der für die Aufnahme in den Rückruf der [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion ausgewertet werden soll.

</dd> <dt>

 Argumente \[ in, optional\]
</dt> <dd>

Daten, die im *dynamicgrouparser* -Parameter des Aufrufes [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) oder [**authzcachedaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)übergeben werden.

</dd> <dt>

*pbaceanwendbar* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine boolesche Variable, die die Ergebnisse der Auswertung der von der Anwendung definierten Logik empfängt.

Die Ergebnisse sind **true** , wenn die Logik festlegt, dass der ACE anwendbar ist und in den [**callzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)-Befehl eingeschlossen wird. Andernfalls sind die Ergebnisse **false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion **true** zurück.

Wenn die Funktion die Auswertung nicht ausführen kann, wird **false** zurückgegeben. Verwenden Sie [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , um einen Fehler an die Access Check-Funktion zurückzugeben.

## <a name="remarks"></a>Bemerkungen

Sicherheits Attribut Variablen müssen im Client Kontext vorhanden sein, wenn Sie in einem bedingten Ausdruck referenziert werden. andernfalls wird der Ausdruck für den bedingten Ausdruck, der auf Sie verweist, zu "unknown" ausgewertet.

Weitere Informationen finden Sie unter [Funktionsweise von Access Check Works](how-dacls-control-access-to-an-object.md) und [zentralisierte Autorisierungs Richtlinien](centralized-authorization-policy.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                   |
| Verteilbare Komponente<br/>          | Windows Server 2003-Verwaltungs Tools Pack unter Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Grundlegende Access Control Funktionen](authorization-functions.md)
</dt> <dt>

[Zentralisierte Autorisierungs Richtlinie](centralized-authorization-policy.md)
</dt> <dt>

[Funktionsweise von Access Check](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**Authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[**Authzcachedaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**Authzinitializeremoteresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**Authzinitializeresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

