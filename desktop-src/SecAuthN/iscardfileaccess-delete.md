---
description: Mit der Delete-Methode wird eine Datei an einem bestimmten Speicherort innerhalb des Smartcard-Dateisystems gelöscht.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: Iscardfileaccess::D Elete-Methode
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
ms.openlocfilehash: 6331225cd3baf105682e2d275ad6be53f16f5b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343599"
---
# <a name="iscardfileaccessdelete-method"></a>Iscardfileaccess::D Elete-Methode

\[Die **Delete** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Mit der **Delete** -Methode wird eine Datei an einem bestimmten Speicherort innerhalb des [*Smartcard*](../secgloss/s-gly.md) -Dateisystems gelöscht.

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

*RefType* \[ in\]
</dt> <dd>

Der Referenztyp, der in *bstrinpathspec* verwendet wird.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**SC- \_ Typ \_ nach \_ Name**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**SC- \_ Typ \_ nach \_ ID**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ - \_ Typ \_ kurz**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC- \_ Typ \_ nach \_ beliebigen**
</dt> </dl> </dd> <dt>

*bstrinpathspec* \[ in\]
</dt> <dd>

Der Bezeichner der zu löschenden Datei.

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Gibt an, ob sicheres Messaging verwendet werden muss und welche Daten vorab zugeordnet werden sollen.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ Secure \_ Messaging**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ FL, \_ vorab zugeordnet**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                  | Beschreibung                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Vorgang wurde erfolgreich abgeschlossen.<br/>          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiger Parameter.<br/>                             |
| <dl> <dt>**E \_ notimpl**</dt> </dl>    | Diese Methode wurde von der-Schnittstelle nicht implementiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

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

[**Stelle**](iscardfileaccess-create.md)
</dt> <dt>

[**Iscardfileaccess**](iscardfileaccess.md)
</dt> </dl>

 

 
