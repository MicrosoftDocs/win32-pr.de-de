---
title: SetSessionDirectoryExposeServerIP-Methode der Win32_TSSessionDirectory-Klasse
description: Legt die SessionDirectoryExposeServerIP-Eigenschaft fest.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- SetSessionDirectoryExposeServerIP-Methode Remotedesktopdienste
- SetSessionDirectoryExposeServerIP-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste , SetSessionDirectoryExposeServerIP-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7267a8462e89bdd995896a97fad82cb84ae4e8a36037e39767eca1239611af29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137603"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a>SetSessionDirectoryExposeServerIP-Methode der Win32 \_ TSSessionDirectory-Klasse

Legt die **SessionDirectoryExposeServerIP-Eigenschaft** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SessionDirectoryExposeServerIP* \[ In\]
</dt> <dd>

Typ: **uint32**

Flag zum Deaktivieren oder Aktivieren der **SessionDirectoryExposeServerIP-Eigenschaft,** die den Abruf der IP-Adresse für das Sitzungsverzeichnis zulässt oder verweigert.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Deaktivieren Sie die -Eigenschaft.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Aktivieren Sie die -Eigenschaft.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Einstellung der Gruppenrichtliniensteuerung unterliegt.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

