---
description: Wird von certdeletectlfromstore aufgerufen, bevor eine CTL aus dem Speicher gelöscht wird.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Certstoreprovdeletectl-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864352"
---
# <a name="certstoreprovdeletectl-callback-function"></a>Certstoreprovdeletectl-Rückruffunktion

Die **certstoreprovdeletectl** -Rückruffunktion wird von [**certdeletectlfromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) aufgerufen, bevor eine CTL aus dem Speicher gelöscht wird. Diese Funktion bestimmt, ob eine CTL gelöscht werden kann.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hstoreprov* \[ in\]
</dt> <dd>

**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).

</dd> <dt>

*pctlcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Alle benötigten Flagwerte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn eine CTL aus dem Speicher gelöscht werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



 

 
