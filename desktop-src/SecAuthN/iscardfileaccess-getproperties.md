---
description: Ruft die primitiven Daten ab, auf die von TLVS (Tag, Länge, Wert) für das angegebene Objekt verwiesen wird.
ms.assetid: 135aeb9a-b851-4522-862f-02a7e020c36b
title: 'Iscardfileaccess:: GetProperties-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 25e6ae1ab657d92dda0ad421b650eaaa7076bd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368846"
---
# <a name="iscardfileaccessgetproperties-method"></a>Iscardfileaccess:: GetProperties-Methode

\[Die **GetProperties** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **GetProperties** -Methode ruft die primitiven Daten ab, auf die von TLVS (Tag, Länge, Wert) für das angegebene Objekt verwiesen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProperties(
  [in]      REFTYPE     refType,
  [in]      BSTR        bstrPathSpec,
  [in]      SCARD_FLAGS flags,
  [in, out] LPTLV_TABLE *ppTLV
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

*bstrinpathspec* \[ in\]
</dt> <dd>

Datei.

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Gibt an, ob sicheres Messaging verwendet werden soll.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ Secure \_ Messaging**
</dt> </dl> </dd> <dt>

*pptlv* \[ in, out\]
</dt> <dd>

Zeiger auf TLV-Strukturen, deren Wert abgerufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>      |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardfileaccess**](iscardfileaccess.md)
</dt> </dl>

 

 
