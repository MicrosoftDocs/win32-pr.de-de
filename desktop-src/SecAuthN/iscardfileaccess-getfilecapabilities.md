---
description: Die getfilefunktionalitäten-Methode ruft eine Liste der Dateifunktionen aus der aktuellen Datei ab.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'Iscardfileaccess:: getfilefunktionen-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216729"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a>Iscardfileaccess:: getfilefunktionen-Methode

\[Die **getfilefunktionen** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **getfilefunktionalitäten** -Methode ruft eine Liste der Dateifunktionen aus der aktuellen Datei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppproperties* \[ in, out\]
</dt> <dd>

Zeiger auf TLV-Strukturen (Tag, length, Wert). Bei der Eingabe gibt dieser Parameter die Dateien an, für die Eigenschaften zu erhalten sind. bei der Ausgabe enthält dieser Parameter die Eigenschaften. Das folgende Beispiel zeigt eine Definition der TLV-Struktur.


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



Weitere Informationen zu TLV-Strukturen finden Sie unter [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .

</dd> <dt>

*plproperties* \[ in, out\]
</dt> <dd>

Zeiger auf die Anzahl der TLV-Einträge in *ppproperties*.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Gibt an, ob sicheres Messaging verwendet werden muss und welche Daten vorab zugeordnet werden sollen.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ Secure \_ Messaging**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ FL, \_ vorab zugeordnet**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                    |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>          |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

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

 

 
