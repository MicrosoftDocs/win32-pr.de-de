---
description: Erstellt eine gültige APDU (Command Application Protocol Data Unit) für die Übertragung an eine Smartcard.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'Iscardcmd:: buildcmd-Methode (scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217168"
---
# <a name="iscardcmdbuildcmd-method"></a>Iscardcmd:: buildcmd-Methode

\[Die **buildcmd** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **buildcmd** -Methode erstellt eine gültige [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) für die Übertragung an eine [*Smartcard*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byclassid* \[ in\]
</dt> <dd>

Befehls Klassen Bezeichner.

</dd> <dt>

*byinsid* \[ in\]
</dt> <dd>

Bezeichner der Befehls Anweisung.

</dd> <dt>

*byP1* \[ in\]
</dt> <dd>

Der erste Parameter des Befehls.

</dd> <dt>

*byP2* \[ in\]
</dt> <dd>

Der zweite Parameter des Befehls.

</dd> <dt>

*pbydata* \[ in\]
</dt> <dd>

Zeiger auf den Daten Teil des Befehls.

</dd> <dt>

*p1Le* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Long Integer-Wert, der die erwartete Länge der zurückgegebenen Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Einer der Parameter ist ungültig.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>        |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Befehl in einem anderen Befehl Kapseln möchten, können Sie [**Kapseln**](iscardcmd-encapsulate.md)einschließen.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardcmd**](iscardcmd.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie ein Befehls-APDU erstellt wird. Im Beispiel wird davon ausgegangen, dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist und dass "pibyterequest" ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist, die mit einem vorherigen Aufrufen der [**ibytebuffer:: Initialize**](ibytebuffer-initialize.md) -Methode initialisiert wurde.


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scarddat. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kapseln**](iscardcmd-encapsulate.md)
</dt> <dt>

[**Iscardcmd**](iscardcmd.md)
</dt> </dl>

 

 
