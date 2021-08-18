---
description: Ruft einen Schnittstellenzeiger auf einen Speicheranbieter ab.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: PStoreCreateInstance-Funktion (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: 2e32319e9585f5d1a80d0473c6ce27167f0ec181b81b974c526371b29c018b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955689"
---
# <a name="pstorecreateinstance-function"></a>PStoreCreateInstance-Funktion

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

\[Diese Funktion kann in zukünftigen Versionen von Windows geändert oder nicht mehr verfügbar sein. Verwenden Sie anstelle dieser Funktion die Funktionen **CryptProtectData** und **CryptUnprotectData.**\]

Ruft einen Schnittstellenzeiger auf einen Speicheranbieter ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppProvider* \[ out\]
</dt> <dd>

Ein Zeiger auf den abgerufenen Schnittstellenzeiger für den Speicheranbieter. Wenn Sie die Verwendung der -Schnittstelle abgeschlossen haben, dekrementieren Sie den Verweiszähler, indem Sie die [**IUnknown::Release-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufrufen. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*pProviderID* \[ In\]
</dt> <dd>

Ein Zeiger auf die **GUID,** die den Speicheranbieter identifiziert. Wenn dieser Parameter **NULL** ist, wird der Basisspeicheranbieter verwendet.

</dd> <dt>

*pReserved* \[ In\]
</dt> <dd>

Reserviert; muss **NULL** sein.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert **S \_ OK** gibt an, dass die Funktion erfolgreich war.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
