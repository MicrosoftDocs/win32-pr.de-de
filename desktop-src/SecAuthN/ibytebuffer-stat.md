---
description: Die Stat-Methode ruft statistische Informationen aus dem Streamobjekt ab.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: IByteBuffer::Stat-Methode (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dd80b408765985b2e009b2e580eb1bf81b08cb5ea1f2e7aaa5ed628a76073a27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127400"
---
# <a name="ibytebufferstat-method"></a>IByteBuffer::Stat-Methode

\[Die **Stat-Methode** ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **Stat-Methode** ruft statistische Informationen aus dem Streamobjekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstatstg* \[ out\]
</dt> <dd>

Zeigt auf eine **STATSTRUCT-Struktur,** in der diese Methode Informationen zu diesem Streamobjekt platziert. Dieser Zeiger ist **NULL,** wenn ein Fehler auftritt.

</dd> <dt>

*grfStatFlag* \[ In\]
</dt> <dd>

Gibt an, dass diese Methode einige der Felder in der **STATSTRUCT-Struktur** nicht zurückgibt, wodurch ein Speicherbelegungsvorgang gespeichert wird. Werte werden aus der [**STATFLAG-Enumeration**](/windows/win32/api/wtypes/ne-wtypes-statflag) übernommen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt an, dass der Aufruf erfolgreich war.

## <a name="remarks"></a>Hinweise

Die **IByteBuffer::Stat-Methode** ruft einen Zeiger auf die **STATSTRUCT-Struktur** ab, die Informationen zu diesem geöffneten Stream enthält.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Abrufen statistischer Informationen aus dem Stream.


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

