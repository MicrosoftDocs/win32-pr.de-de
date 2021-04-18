---
description: Ruft ein Enumeratorobjekt ab, das wiederum zum Auflisten der geschützten Speicher Anbieter verwendet werden kann, die zurzeit auf dem System installiert sind.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Pstoreenumproviders-Funktion (pstore. h)
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
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371459"
---
# <a name="pstoreenumproviders-function"></a>Pstoreenumproviders-Funktion

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Ruft ein Enumeratorobjekt ab, das wiederum zum Auflisten der geschützten Speicher Anbieter verwendet werden kann, die zurzeit auf dem System installiert sind.

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

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*ppum* 
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**ienumpstoreproviders**](ienumpstoreproviders.md) -Schnittstelle, die zum Aufzählen installierter Anbieter verwendet werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt ein **HRESULT** zurück.

## <a name="remarks"></a>Bemerkungen

Die geschützte Speicherkomponente verfügt über eine Anbieter basierte Architektur. Anwendungen, die geschützten Speicher nutzen, können angeben, welche der installierten Anbieter beim Speichern und Abrufen der Daten verwendet werden sollen.

Die **pstoreenumproviders** -Funktion wird zum Auflisten der installierten geschützten Speicher Anbieter verwendet. Jeder Anbieter wird durch einen Globally Unique Identifier (GUID) identifiziert.

Bis zu diesem Zeitpunkt wurde immer nur ein geschützter Speicher Anbieter geschrieben. Da der geschützte Speicherdienst zurzeit veraltet ist, ist es sehr unwahrscheinlich, dass jemals weitere Anbieter erstellt werden. Daher sollte diese Funktion nicht für beliebige Zwecke verwendet werden.

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumpstoreproviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
