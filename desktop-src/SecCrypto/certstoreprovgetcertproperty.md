---
description: Ruft eine angegebene Eigenschaft eines Zertifikats ab.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Certstoreprovgetcertproperty-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362420"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a>Certstoreprovgetcertproperty-Rückruffunktion

Die **certstoreprovgetcertproperty** -Rückruffunktion Ruft eine angegebene Eigenschaft eines Zertifikats ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
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

*pcertcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur.

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

Ein Zeiger auf einen Puffer, der den Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur enthalten soll, die von der Funktion zurückgegeben werden soll. Kann bei einem ersten Aufrufe der-Funktion auf **null** festgelegt werden, um den Wert von *pcbData* abzurufen, bevor für den Pufferspeicher zugewiesen wird.

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

[**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
