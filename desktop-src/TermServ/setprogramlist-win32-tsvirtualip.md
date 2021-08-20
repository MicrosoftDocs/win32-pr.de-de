---
title: SetProgramList-Methode der Win32_TSVirtualIP Klasse
description: Überschreibt die Liste der Programme, die IP-Virtualisierung verwenden.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- SetProgramList-Remotedesktopdienste
- SetProgramList-Methode Remotedesktopdienste , Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP klasse Remotedesktopdienste , SetProgramList-Methode
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
ms.openlocfilehash: 22ac74ca1a718fe1ec3c561b70da935d00a15f1bcb040cb29464ed9b6e52195c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349606"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a>SetProgramList-Methode der Win32 \_ TSVirtualIP-Klasse

Überschreibt die Liste der Programme, die IP-Virtualisierung verwenden.

## <a name="syntax"></a>Syntax


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProgramList* \[ In\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Ein Array von Zeichenfolgen, die den Pfad und die Dateinamen der Programme enthalten, die IP-Virtualisierung verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **unint32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter. Die -Methode gibt einen Fehler zurück, wenn sich die Einstellung unter der Gruppenrichtliniensteuerung befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





