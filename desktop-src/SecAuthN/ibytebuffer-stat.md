---
description: Die Stat-Methode ruft statistische Informationen aus dem Streamobjekt ab.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'Ibytebuffer:: Stat-Methode (scardssp. h)'
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
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349632"
---
# <a name="ibytebufferstat-method"></a>Ibytebuffer:: Stat-Methode

\[Die **stat** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **stat** -Methode ruft statistische Informationen aus dem Streamobjekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstatus* \[ vorgenommen\]
</dt> <dd>

Verweist auf eine **Status** Struktur, in der diese Methode Informationen zu diesem Streamobjekt platziert. Dieser Zeiger ist **null** , wenn ein Fehler auftritt.

</dd> <dt>

*grsstatflag* \[ in\]
</dt> <dd>

Gibt an, dass diese Methode einige der Felder in der Struktur der **Status** Struktur nicht zurückgibt, wodurch ein Speicher Belegungs Vorgang gespeichert wird. Werte werden aus der [**StatFlag**](/windows/win32/api/wtypes/ne-wtypes-statflag) -Enumeration entnommen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Die **ibytebuffer:: stat** -Methode ruft einen Zeiger auf die **statstruct** -Struktur ab, die Informationen zu diesem geöffneten Stream enthält.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie statistische Informationen aus dem Stream abgerufen werden.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

