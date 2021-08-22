---
title: GetTSLanaIds-Methode der Win32_TerminalServiceSetting-Klasse
description: Ruft die LANA-IDs (NetBIOS Local Area Network Adapter) und Beschreibungen Remotedesktopdienste Netzwerkadaptern ab.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- GetTSLanaIds-Remotedesktopdienste
- GetTSLanaIds-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting klasse Remotedesktopdienste , GetTSLanaIds-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c96c840879013f86339cd17136ea97a6c3da9933b1e409cf160779908e4038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059578"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a>GetTSLanaIds-Methode der Win32 \_ TerminalServiceSetting-Klasse

Die **GetTSLanaIds-Methode** ruft die LANA-IDs (NetBIOS Local Area Network Adapter) und Beschreibungen Remotedesktopdienste Netzwerkadaptern ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LanaIdList* \[ out\]
</dt> <dd>

Array von LANA-Nummern.

</dd> <dt>

*LanaIdDescriptions* \[ out\]
</dt> <dd>

Array von LANA-Beschreibungen, die dem *LanaIdList-Array* entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

