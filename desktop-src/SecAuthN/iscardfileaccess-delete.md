---
description: Die Delete-Methode löscht eine Datei an einem bestimmten Speicherort im Smartcarddateisystem.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: ISCardFileAccess::D elete-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 721830ea3d446585e7f52c699642b1534c78d34826722b5737e191dfce94c817
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008048"
---
# <a name="iscardfileaccessdelete-method"></a>ISCardFileAccess::D elete-Methode

\[Die **Delete-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **Delete-Methode** löscht eine Datei an einem bestimmten Speicherort im [*Smartcarddateisystem.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*refType* \[ In\]
</dt> <dd>

Typ des Verweises, der in *bstrPathSpec* verwendet wird.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**SC \_ TYPE \_ BY \_ NAME**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**SC \_ TYPE \_ BY \_ ID**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ TYPE \_ BY \_ SHORT**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ TYPE \_ BY \_ ANY**
</dt> </dl> </dd> <dt>

*bstrPathSpec* \[ In\]
</dt> <dd>

Bezeichner der zu löschenden Datei.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Gibt an, ob sicheres Messaging verwendet und Daten vorab zugeordnet werden müssen.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ SECURE \_ MESSAGING**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**\_SC FL VORAB \_ ZUGEORDNET**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Vorgang wurde erfolgreich abgeschlossen.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültiger Parameter.<br/>                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Die -Schnittstelle hat diese Methode nicht implementiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardFileAccess.**](iscardfileaccess.md)

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen Smartcardfehlercode zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Erstellen**](iscardfileaccess-create.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
