---
description: Die Write-Methode schreibt Daten in eine aktuell geöffnete Datei.
ms.assetid: 0c92af34-a9db-4242-8b6e-d1010a0d7afa
title: ISCardFileAccess::Write-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: c48f900ad5026af61cfc5b4f68c7908bd77881a637082a3fe1d05bc7c72f4b51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923179"
---
# <a name="iscardfileaccesswrite-method"></a>ISCardFileAccess::Write-Methode

\[Die **Write-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **Write-Methode** schreibt Daten in eine aktuell geöffnete Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT Write(
  [in] HSCARD_FILE  hFile,
  [in] LPBYTEBUFFER pData,
  [in] SCARD_FLAGS  flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFile* \[ In\]
</dt> <dd>

Ein Handle für eine geöffnete Datei.

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Zu schreibende Objekte/Daten.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Gibt an, ob sicheres Messaging verwendet werden soll.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ SECURE \_ MESSAGING**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde übergeben.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Um eine Datei zu öffnen oder zu schließen, rufen [**Sie Öffnen**](iscardfileaccess-open.md) bzw. [**Schließen**](iscardfileaccess-close.md)auf.

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardFileAccess.**](iscardfileaccess.md)

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen [*Smartcardfehlercode*](../secgloss/s-gly.md) zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schließen**](iscardfileaccess-close.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Öffnen**](iscardfileaccess-open.md)
</dt> </dl>

 

 
