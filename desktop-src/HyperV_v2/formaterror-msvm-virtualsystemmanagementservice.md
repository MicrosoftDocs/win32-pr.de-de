---
description: Gibt eine formatierte Fehlermeldungszeichenfolge für das angegebene Array eingebetteter \_ Msvm-Fehlerinstanzen zurück.
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: FormatError-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31b7f2ba03c21c08af3b9249c0ee3099291fdd190d22516ed503c012dae63f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253950"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a>FormatError-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Gibt eine formatierte Fehlermeldungszeichenfolge für das angegebene Array eingebetteter [**\_ Msvm-Fehlerinstanzen**](msvm-error.md) zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ In\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Ein Array von Zeichenfolgen, die [**Msvm \_ Error-Instanzen**](msvm-error.md) enthalten, die zum Generieren der Ausgabefehlermeldung verwendet werden.

</dd> <dt>

*ErrorMessage* \[ out\]
</dt> <dd>

Typ: **Zeichenfolge**

Bei der Ausgabe eine Zeichenfolge, die die verketteten Fehlermeldungen enthält, die durch die [**msvm-Fehlerinstanzen \_**](msvm-error.md) dargestellt werden, die im *Errors-Parameter* übergeben werden. Jede Fehlerzeichenfolge wird durch ein Paar von Neulinienzeichen (' \\ n') getrennt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FormatError (V1)**](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

