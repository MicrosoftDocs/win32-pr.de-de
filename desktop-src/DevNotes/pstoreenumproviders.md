---
description: Ruft ein Enumeratorobjekt ab, das wiederum zum Aufzählen der geschützten Speicheranbieter verwendet werden kann, die derzeit auf dem System installiert sind.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: PStoreEnumProviders-Funktion (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: d2e0b77e0c68864b068f9c5476ca117ca039224a709ebcad83b22f31f908c26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541560"
---
# <a name="pstoreenumproviders-function"></a>PStoreEnumProviders-Funktion

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

Ruft ein Enumeratorobjekt ab, das wiederum zum Aufzählen der geschützten Speicheranbieter verwendet werden kann, die derzeit auf dem System installiert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*ppenum* 
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IEnumPStoreProviders-Schnittstelle,**](ienumpstoreproviders.md) mit der installierte Anbieter aufzählt werden können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt ein **HRESULT zurück.**

## <a name="remarks"></a>Hinweise

Die geschützte Speicherkomponente verfügt über eine anbieterbasierte Architektur. Anwendungen, die geschützten Speicher verwenden, können angeben, welche der installierten Anbieter beim Speichern und Abrufen ihrer Daten verwendet werden.

Die **PStoreEnumProviders-Funktion** wird verwendet, um die installierten geschützten Speicheranbieter aufzählen. Jeder Anbieter wird durch einen global eindeutigen Bezeichner (Globally Unique Identifier, GUID) identifiziert.

Bis zu diesem Zeitpunkt wurde nur ein geschützter Speicheranbieter geschrieben. Da der geschützte Speicherdienst derzeit veraltet ist, ist es sehr unwahrscheinlich, dass weitere Anbieter erstellt werden. Daher sollte diese Funktion nicht für irgendeinen Zweck verwendet werden.

Dieser Funktion ist keine Importbibliothek zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
