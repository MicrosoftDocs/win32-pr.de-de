---
description: Mit der changedir-Methode wird das aktuelle Smartcardverzeichnis in das neue angegebene Verzeichnis geändert.
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: 'Iscardfileaccess:: changedir-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 147456bd705eea3073f2e65cb375494187ca2473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862628"
---
# <a name="iscardfileaccesschangedir-method"></a>Iscardfileaccess:: changedir-Methode

\[Die **changedir** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Mit der **changedir** -Methode wird das aktuelle [*Smartcardverzeichnis*](../secgloss/s-gly.md) in das neue angegebene Verzeichnis geändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RefType* \[ in\]
</dt> <dd>

Der Referenztyp, der in *bstrinnewdir* verwendet wird.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**SC- \_ Typ \_ nach \_ Name**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**SC- \_ Typ \_ nach \_ ID**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ - \_ Typ \_ kurz**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC- \_ Typ \_ nach \_ beliebigen**
</dt> </dl> </dd> <dt>

*bstrinnewdir* \[ in\]
</dt> <dd>

Der Datei-/Verzeichnisname (von *RefType*), der ausgewählt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Um einen absoluten Pfad zum aktuell ausgewählten Verzeichnis abzurufen, nennen Sie [**getcurrentdir**](iscardfileaccess-getcurrentdir.md).

Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getcurrentdir**](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[**Iscardfileaccess**](iscardfileaccess.md)
</dt> </dl>

 

 
