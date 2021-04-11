---
description: Die CopyTo-Methode kopiert eine angegebene Anzahl von Bytes vom aktuellen Such Zeiger im-Objekt in den aktuellen Such Zeiger in einem anderen-Objekt.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'Ibytebuffer:: CopyTo-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217779"
---
# <a name="ibytebuffercopyto-method"></a>Ibytebuffer:: CopyTo-Methode

\[Die **CopyTo** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **CopyTo** -Methode kopiert eine angegebene Anzahl von Bytes vom aktuellen Such Zeiger im-Objekt in den aktuellen Such Zeiger in einem anderen-Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbytebuffer* \[ in\]
</dt> <dd>

Verweist auf den Zielstream. Der Stream, auf den *pbytebuffer* zeigt, kann ein neuer Datenstrom oder ein Klon des Quelldaten Stroms sein.

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Anzahl der Bytes, die aus dem Quelldaten Strom kopiert werden sollen.

</dd> <dt>

*pcbread* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Speicherort, an dem diese Methode die tatsächliche Anzahl von Bytes schreibt, die aus der Quelle gelesen wurden. Sie können diesen Zeiger auf **null** festlegen, um anzugeben, dass dieser Wert nicht von Interesse ist. In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der gelesenen Bytes bereit.

</dd> <dt>

*pcbwritten* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Speicherort, an dem diese Methode die tatsächliche Anzahl von Bytes schreibt, die in das Ziel geschrieben werden. Sie können diesen Zeiger auf **null** festlegen, um anzugeben, dass dieser Wert nicht von Interesse ist. In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der geschriebenen Bytes bereit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.

## <a name="remarks"></a>Bemerkungen

Diese Methode kopiert die angegebenen Bytes von einem Stream in einen anderen. Sie kann auch verwendet werden, um einen Datenstrom in sich selbst zu kopieren. Der Such Zeiger in jeder Stream-Instanz wird für die Anzahl der gelesenen oder geschriebenen Bytes angepasst.

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



 

