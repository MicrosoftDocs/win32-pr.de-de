---
description: Ruft einen Schnittstellen Zeiger auf einen Speicher Anbieter ab.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Pstorecreateinstance-Funktion (pstore. h)
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
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358132"
---
# <a name="pstorecreateinstance-function"></a>Pstorecreatanstance-Funktion

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

\[Diese Funktion kann in zukünftigen Versionen von Windows geändert werden oder nicht verfügbar sein. Verwenden Sie anstelle dieser Funktion die Funktionen " **CryptProtectData** " und " **CryptUnprotectData** ".\]

Ruft einen Schnittstellen Zeiger auf einen Speicher Anbieter ab.

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

*ppprovider* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den abgerufenen Schnittstellen Zeiger für den Speicher Anbieter. Wenn Sie die-Schnittstelle verwenden, verringern Sie den Verweis Zähler, indem Sie die [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode aufrufen. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*pproviderid* \[ in\]
</dt> <dd>

Ein Zeiger auf die **GUID** , die den Speicher Anbieter identifiziert. Wenn dieser Parameter **null** ist, wird der Basis Speicher Anbieter verwendet.

</dd> <dt>

*beibehalten* \[ in\]
</dt> <dd>

Bleiben muss **null** sein.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert **S \_ OK** gibt an, dass die Funktion erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
