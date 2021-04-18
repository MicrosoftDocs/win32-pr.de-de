---
description: Ruft eine angegebene Eigenschaft einer CRL ab.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Certstoreprovgetcrlproperty-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357511"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>Certstoreprovgetcrlproperty-Rückruffunktion

Die **certstoreprovgetcrlproperty** -Rückruffunktion Ruft eine angegebene Eigenschaft einer [*CRL*](../secgloss/c-gly.md)ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
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

Ein Zeiger auf eine [**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) Struktur.

</dd> <dt>

*dwpropid* \[ in\]
</dt> <dd>

Gibt einen Eigenschafts Bezeichner an.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Alle benötigten Flagwerte.

</dd> <dt>

*pvData* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Zeiger auf eine [**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) Struktur enthalten soll, die von der Funktion zurückgegeben werden soll. Kann bei einem ersten Aufrufe der-Funktion auf **null** festgelegt werden, um den Wert von *pcbData* abzurufen, bevor für den Pufferspeicher zugewiesen wird.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Ein Zeiger auf ein **DWORD** , das die Länge des *pvData* -Puffers angibt.

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

[**CRL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
