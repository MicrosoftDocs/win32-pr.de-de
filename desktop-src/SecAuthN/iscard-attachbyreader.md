---
description: Die AttachByReader-Methode öffnet die Smartcard im benannten Reader.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: ISCard::AttachByReader-Methode (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1227c94edbf5816a8f1e867436462a743e6961e3ca70bb7b8a521c289312f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015680"
---
# <a name="iscardattachbyreader-method"></a>ISCard::AttachByReader-Methode

\[Die **AttachByReader-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **AttachByReader-Methode** öffnet die [*Smartcard*](../secgloss/s-gly.md) im benannten [*Reader*](../secgloss/r-gly.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrReaderName* \[ In\]
</dt> <dd>

Ein **BSTR,** der den Namen des Smartcardlesers enthält.

</dd> <dt>

*ShareMode* \[ In\]
</dt> <dd>

Modus, in dem der Zugriff auf die Smartcard beansprucht werden soll.



| Wert                                                                                                                                            | Bedeutung                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Exklusive**</dt> </dl> | Niemand anderes verwendet diese Verbindung mit der Smartcard.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**geteilt**</dt> </dl>          | Andere Anwendungen können diese Verbindung verwenden.<br/>        |



 

</dd> <dt>

*PrefProtocol* \[ In\]
</dt> <dd>

Bevorzugter Protokollwert.

<dl><span id="T0"></span><span id="t0"></span><dt>

**T0**
</dt><span id="T1"></span><span id="t1"></span><dt>

**T1**
</dt><span id="RAW"></span><span id="raw"></span><dt>

**RAW**
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

**T0 \| T1**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Das Öffnen auf der Smartcard im benannten Reader wurde erfolgreich abgeschlossen.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Es liegt ein Problem mit einem oder mehreren parametern vor, die an die Funktion übergeben werden.<br/> |



 

## <a name="remarks"></a>Hinweise

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen [*Smartcardfehlercode*](../secgloss/s-gly.md) zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

Wenn Sie die Verwendung des Readers abgeschlossen haben, geben Sie die Anlage frei, indem Sie die [**ISCard::D etach-Methode**](iscard-detach.md) aufrufen.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Anfügen an eine Smartcard in einem angegebenen Smartcardleser.


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard ist als 1461AAC3-6810-11D0-918F-00AA00C18068 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**Trennen**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**Anfügen**](iscard-reattach.md)
</dt> </dl>

 

 
