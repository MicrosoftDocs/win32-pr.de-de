---
description: Ruft eine angegebene Eigenschaft einer Zertifikat Vertrauens Liste (Certificate Trust List, CTL) ab.
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Certstoreprovgetctlproperty-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368936"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>Certstoreprovgetctlproperty-Rückruffunktion

Die **certstoreprovgetctlproperty** -Rückruffunktion Ruft eine angegebene Eigenschaft einer [*Zertifikat Vertrauens Liste (Certificate Trust List*](../secgloss/c-gly.md) , CTL) ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
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

Ein **hcertstoreprov** -Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md).

</dd> <dt>

*pctlcontext* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur.

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

Ein Zeiger auf einen Puffer, der den Zeiger auf eine [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) Struktur enthalten soll, die von der Funktion zurückgegeben werden soll. Dieser Parameter kann bei einem ersten Aufrufen der-Funktion auf **null** festgelegt werden, um den Wert von *pcbData* vor der Zuweisung von Arbeitsspeicher für den Puffer zu erhalten.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Ein Zeiger auf ein **DWORD** , das die Länge des *pvData* -Puffers angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion einen Wert ungleich NULL zurück.

Wenn die Funktion fehlschlägt, gibt Sie 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
