---
description: Die attachbyreader-Methode öffnet die Smartcard im benannten Reader.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'Iscard:: attachbyreader-Methode (scardmgr. h)'
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
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960540"
---
# <a name="iscardattachbyreader-method"></a>Iscard:: attachbyreader-Methode

\[Die **attachbyreader** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **attachbyreader** -Methode öffnet die [*Smartcard*](../secgloss/s-gly.md) im benannten [*Reader*](../secgloss/r-gly.md).

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

*bstrinreadername* \[ in\]
</dt> <dd>

Ein **BSTR** -Wert, der den Namen des smartcardreaders enthält.

</dd> <dt>

*Share Mode* \[ in\]
</dt> <dd>

Der Modus, in dem der Zugriff auf die Smartcard beansprucht werden soll.



| Wert                                                                                                                                            | Bedeutung                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Ausschließliche**</dt> </dl> | Diese Verbindung wird von keiner anderen Person mit der Smartcard verwendet.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**Genu**</dt> </dl>          | Diese Verbindung kann von anderen Anwendungen verwendet werden.<br/>        |



 

</dd> <dt>

*Präfetokoll* \[ in\]
</dt> <dd>

Bevorzugter Protokoll Wert.

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

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Das Öffnen auf der Smartcard im benannten Reader wurde erfolgreich abgeschlossen.<br/>           |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Bei einem oder mehreren Parametern, die an die Funktion weitergegeben wurden, ist ein Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

Wenn Sie die Verwendung des Readers abgeschlossen haben, geben Sie die Anlage frei, indem Sie die [**iscard::D Etach**](iscard-detach.md) -Methode aufrufen.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt das Anfügen an eine Smartcard in einem angegebenen Smartcardlesegerät.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardmgr. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscard ist definiert als 1461aac3-6810-11D0-918f -00aa00c18068<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attachbyhandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**Trennen**](iscard-detach.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> <dt>

[**Erneut**](iscard-reattach.md)
</dt> </dl>

 

 
