---
description: Wird aufgerufen, wenn das vom certstoreprovfindctl-Rückruf zurückgegebene Zertifikat in einem nachfolgenden Aufruf von certstoreprovfindctl nicht verwendet und daher freigegeben wurde.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Certstoreprovfrefindctl-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362421"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>Certstoreprovfrefindctl-Rückruffunktion

Die **certstoreprovfrefindctl** -Rückruffunktion wird aufgerufen, wenn das vom [**certstoreprovfindctl**](certstoreprovfindctl.md) -Rückruf zurückgegebene Zertifikat nicht verwendet und daher in einem nachfolgenden Aufruf von " **certstoreprovfindctl**" freigegeben wurde. Bevor der Close-Rückruf aufgerufen wird, müssen alle vom [**certstoreprovfindctl**](certstoreprovfindctl.md) -Rückruf zurückgegebenen Zertifikate vom Anbieter mithilfe von **certstoreprovfindctl** oder **certstoreprovfreifindctl** freigegeben werden.

## <a name="syntax"></a>Syntax


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
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

*pctlcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur.

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

[**Certstoreprovfindctl**](certstoreprovfindctl.md)
</dt> <dt>

[**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
