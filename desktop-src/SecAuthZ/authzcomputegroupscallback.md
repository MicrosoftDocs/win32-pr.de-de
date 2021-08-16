---
description: Eine anwendungsdefinierte Funktion, die eine Liste von Sicherheits-IDs (SIDs) erstellt, die für einen Client gelten. HzComputeGroupsCallback ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: HzComputeGroupsCallback-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7c30194e4131cbd375192723e23308e1ad5ead69d849ab73857f72ef1d4b0790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784078"
---
# <a name="authzcomputegroupscallback-callback-function"></a>HzComputeGroupsCallback-Rückruffunktion

Die **Funktion "ComputeGroupsCallback"** ist eine anwendungsdefinierte Funktion, die eine Liste von Sicherheits-IDs (SIDs) erstellt, die für einen Client gelten. [](/windows/desktop/SecGloss/s-gly) **HzComputeGroupsCallback** ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hAuthzClientContext* \[ In\]
</dt> <dd>

Ein Handle für einen Clientkontext.

</dd> <dt>

*Args* \[ In\]
</dt> <dd>

Daten, die im *DynamicGroupArgs-Parameter* eines Aufrufs der [**Funktion "AuthhzInitializeContextFromAuthzContext",**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) [**"AuthhzInitializeContextFromSid"**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)oder [**"AuthhzInitializeContextFromToken"**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) übergeben werden.

</dd> <dt>

*pSidAttrArray* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Zeigervariable, die die Adresse eines Arrays von [**\_ SID- und \_ ATTRIBUTES-Strukturen empfängt.**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Diese Strukturen stellen die Gruppen dar, zu denen der Client gehört.

</dd> <dt>

*pSidCount* \[ out\]
</dt> <dd>

Die Anzahl der Strukturen in *pSidAttrArray.*

</dd> <dt>

*pRestrictedSidAttrArray* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Zeigervariable, die die Adresse eines Arrays von [**\_ SID- und \_ ATTRIBUTES-Strukturen empfängt.**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Diese Strukturen stellen die Gruppen dar, von denen der Client eingeschränkt ist.

</dd> <dt>

*pRestrictedSidCount* \[ out\]
</dt> <dd>

Die Anzahl der Strukturen in *pSidRestrictedAttrArray.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich eine Liste von SIDs zurückgibt, ist der Rückgabewert **TRUE.**

Wenn die Funktion fehlschlägt, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Anwendungen können dem Clientkontext auch SIDs hinzufügen, indem [**sie PerlhzAddSidsToContext aufrufen.**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)

Attributvariablen müssen in Form eines Ausdrucks sein, wenn sie mit logischen Operatoren verwendet werden. Andernfalls werden sie als unbekannt ausgewertet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                   |
| Verteilbare Komponente<br/>          | Windows Server 2003 Administration Tools Pack on Windows XP<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Grundlegende Access Control Funktionen](authorization-functions.md)
</dt> <dt>

[**HzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[**AuhzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthhzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[**QshzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[**QshzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[**QshzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[**SID \_ UND \_ ATTRIBUTE**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

