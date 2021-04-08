---
description: Eine Anwendungs definierte Funktion, die eine Liste von Sicherheits-IDs (SIDs) erstellt, die für einen Client gelten. Authzcomputegroupscallback ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Authzcomputegroupscallback-Rückruffunktion
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
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760830"
---
# <a name="authzcomputegroupscallback-callback-function"></a>Authzcomputegroupscallback-Rückruffunktion

Die **authzcomputegroupscallback** -Funktion ist eine Anwendungs definierte Funktion, die eine Liste von [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs) erstellt, die für einen Client gelten. **Authzcomputegroupscallback** ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.

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

" *hauthzclientcontext* \[ " in\]
</dt> <dd>

Ein Handle für einen Client Kontext.

</dd> <dt>

*Args* \[ in\]
</dt> <dd>

Daten, die im *dynamicgrouparser* -Parameter eines Aufrufes der [**authzinitializecontextfromauthzcontext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)-, [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)-oder [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) -Funktion übergeben werden.

</dd> <dt>

*psidattrarray* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeiger Variable, die die Adresse eines Arrays von [**sid \_ -und \_ Attribute-**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Strukturen empfängt. Diese Strukturen stellen die Gruppen dar, zu denen der Client gehört.

</dd> <dt>

*psidcount* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Strukturen in *psidattrarray*.

</dd> <dt>

*prestrictedsidattrarray* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeiger Variable, die die Adresse eines Arrays von [**sid \_ -und \_ Attribute-**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Strukturen empfängt. Diese Strukturen stellen die Gruppen dar, von denen der Client beschränkt ist.

</dd> <dt>

*prestrictedsidcount* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Strukturen in *psidrestrictedattrarray*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich eine Liste von SIDs zurückgibt, ist der Rückgabewert " **true**".

Wenn die Funktion fehlschlägt, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Anwendungen können dem Client Kontext auch SIDs hinzufügen, indem Sie [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)aufrufen.

Attribut Variablen müssen in Form eines Ausdrucks vorliegen, wenn Sie mit logischen Operatoren verwendet werden. Andernfalls werden Sie als UNKNOWN ausgewertet.

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

[**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[**Authzcachedaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**Authzinitializecontextfromauthzcontext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[**Authzinitializeresourcemanager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[**SID \_ und \_ Attribute**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

