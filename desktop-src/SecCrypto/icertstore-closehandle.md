---
description: Schließt ein HCERTSTORE-Handle, das über die StoreHandle-Eigenschaft erworben wurde.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: ICertStore::CloseHandle-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3d6f1b0b44cd0fdc71f8f3d37fa9bd8290c5d606eea1f97f5bf6644f9ce8e2a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005658"
---
# <a name="icertstoreclosehandle-method"></a>ICertStore::CloseHandle-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **CloseHandle-Methode** schließt ein HCERTSTORE-Handle, das über die [**StoreHandle-Eigenschaft erworben**](icertstore-storehandle.md) wurde.

## <a name="syntax"></a>Syntax


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hCertStore* \[ In\]
</dt> <dd>

Das zu schließende HCERTSTORE-Handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert **S OK gibt \_ den** Erfolg an. Jeder andere Wert gibt an, dass der Vorgang fehlgeschlagen ist.

## <a name="remarks"></a>Hinweise

Diese Methode gibt nicht das HCERTSTORE-Handle frei, das in einem [**Store**](store.md) ist. Es sollte nur verwendet werden, um ein HCERTSTORE-Handle frei zu geben, das über die [**StoreHandle-Eigenschaft erworben**](icertstore-storehandle.md) wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




