---
title: Setprogramlist-Methode der Win32_TSVirtualIP-Klasse
description: Überschreibt die Liste der Programme, die die IP-Virtualisierung verwenden.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Setprogramlist-Methode Remotedesktopdienste
- Setprogramlist-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, setprogramlist-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518023"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a>Setprogramlist-Methode der Win32- \_ Klasse "tvirtualip"

Überschreibt die Liste der Programme, die die IP-Virtualisierung verwenden.

## <a name="syntax"></a>Syntax


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Programmliste* \[ in\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Ein Array von Zeichen folgen, das die Pfad-und Dateinamen der Programme enthält, die die IP-Virtualisierung verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **unint32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ virtualialip**](win32-tsvirtualip.md)
</dt> </dl>

 

 





