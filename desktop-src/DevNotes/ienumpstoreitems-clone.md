---
description: 'IEnumPStoreItems::Clone-Methode: Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.'
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: IEnumPStoreItems::Clone-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 29b618881305296a560dc9102f7571c08236d1bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089328"
---
# <a name="ienumpstoreitemsclone-method"></a>IEnumPStoreItems::Clone-Methode

\[Geschützter Speicher (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppenum* \[ out\]
</dt> <dd>

Ein Zeiger auf einen [**IEnumPStoreItems-Zeiger.**](ienumpstoreitems.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT-Wert.**

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> </dl>

 

 
