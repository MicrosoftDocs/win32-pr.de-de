---
description: Wird aufgerufen, wenn das vom certstoreprovfindcrl-Rückruf zurückgegebene Zertifikat in einem nachfolgenden Aufruf von certstoreprovfindcrl nicht verwendet und daher freigegeben wurde.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Certstoreprovfrefindcrl-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867168"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>Certstoreprovfrefindcrl-Rückruffunktion

Die **certstoreprovfrefindcrl** -Rückruffunktion wird aufgerufen, wenn das vom [**certstoreprovfindcrl**](certstoreprovfindcrl.md) -Rückruf zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von **certstoreprovfindcrl** freigegeben wurde. Bevor der schließende Rückruf aufgerufen wird, müssen alle vom [**certstoreprovfindcrl**](certstoreprovfindcrl.md) -Rückruf zurückgegebenen Zertifikate vom Anbieter mithilfe von **certstoreprovfindcrl** oder **certstoreprovfreifindcrl** freigegeben werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hstoreprov* \[ in\]
</dt> <dd>

**Hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).

</dd> <dt>

*pcrlcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf einen [**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

</dd> <dt>

*pvstoreprovfindinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der Informationen zu suchen enthält.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Alle benötigten Flagwerte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Funktion erfolgreich ist, oder **false** , wenn Sie fehlschlägt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Certstoreprovfindcrl**](certstoreprovfindcrl.md)
</dt> <dt>

[**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
