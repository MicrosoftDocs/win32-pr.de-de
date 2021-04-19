---
description: Gibt eine formatierte Fehlermeldungs Zeichenfolge für das angegebene Array von eingebetteten MSVM- \_ Fehler Instanzen zurück.
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Formaterror-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346974"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Formaterror-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Gibt eine formatierte Fehlermeldungs Zeichenfolge für das angegebene Array von eingebetteten [**MSVM- \_ Fehler**](msvm-error.md) Instanzen zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ in\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Ein Array von Zeichen folgen mit [**MSVM- \_ Fehler**](msvm-error.md) Instanzen, die zum Generieren der Ausgabe Fehlermeldung verwendet werden.

</dd> <dt>

*ErrorMessage* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichenfolge**

Bei Ausgabe eine Zeichenfolge, die die verketteten Fehlermeldungen enthält, die von den [**MSVM- \_ Fehler**](msvm-error.md) Instanzen dargestellt werden, die im *Errors* -Parameter übergeben werden. Jede Fehler Zeichenfolge wird durch ein Zeilen Zeilenpaar (" \\ n") getrennt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Formaterror (v1)**](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

