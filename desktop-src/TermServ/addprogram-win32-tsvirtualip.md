---
title: AddProgram-Methode der Win32_TSVirtualIP -Klasse (Bdaiface.h)
description: Fügt der Liste der Programme, die IP-Virtualisierung verwenden, ein Programm hinzu.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- AddProgram-Remotedesktopdienste
- AddProgram-Methode Remotedesktopdienste , Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP klasse Remotedesktopdienste , AddProgram-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2f78cb461a61467867a544e954a71c23d59432e29450a7b0f35184f0edec57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757858"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a>AddProgram-Methode der Win32 \_ TSVirtualIP-Klasse

Fügt der Liste der Programme, die IP-Virtualisierung verwenden, ein Programm hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProgramPath* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Der Pfad und Dateiname des Programms, das der Liste hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter. Die -Methode gibt einen Fehler zurück, wenn sich die Einstellung unter der Gruppenrichtliniensteuerung befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| Header<br/>                   | <dl> <dt>Bdaiface.h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





