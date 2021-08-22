---
description: Legt das HCERTSTORE-Handle eines Zertifikatspeichers fest oder ruft es ab.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: ICertStore::StoreHandle (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2858e7484c82663b2ba6866d0f17b5528921619dbfa80cbb76ec0eabbb39a332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005618"
---
# <a name="icertstorestorehandle-property"></a>ICertStore::StoreHandle (Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **StoreHandle-Eigenschaft** legt das HCERTSTORE-Handle eines Zertifikatspeichers fest oder ruft es ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a>Eigenschaftswert

Das HCERTSTORE-Handle des Zertifikatspeichers.

## <a name="error-codes"></a>Fehlercodes

Wenn die Eigenschaftenzugriffsmethoden **\_ StoreHandle und** **get \_ StoreHandle** erfolgreich verwenden, geben sie S \_ OK zurück.

Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="remarks"></a>Hinweise

Sie müssen entweder die [**CloseHandle-Methode**](icertstore-closehandle.md) oder die [**CertCloseStore-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) aufrufen, um den Kontext frei zu geben.

Wenn Sie die **StoreHandle-Eigenschaft** festlegen, wird der Zustand des gesamten Store [**zurückgesetzt.**](store.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




