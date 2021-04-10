---
title: Die Methode "szessiondirectoryexposeserverip" der Win32_TSSessionDirectory-Klasse
description: Legt die sessiondirectoriyexposeserverip-Eigenschaft fest.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "" der Methode "" der Methode "*"
- Methode Remotedesktopdienste der Methode "" der Klasse "Win32_TSSessionDirectory"
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, Methode "" der Methode ""
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
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949732"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a>Die Methode "tssessiondirectoryexposeserverip" der Win32- \_ Klasse "tssessiondirectory"

Legt die **sessiondirectoriyexposeserverip-** Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sessiondirectoriyexposeserverip* \[ in\]
</dt> <dd>

Typ: **UInt32**

Flag zum Deaktivieren oder Aktivieren der **sessiondirectoriyexposeserverip-** Eigenschaft, die das Abrufen der IP-Adresse für das Sitzungs Verzeichnis zulässt oder ablehnt.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Deaktivieren Sie die-Eigenschaft.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Aktivieren Sie die-Eigenschaft.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tssessiondirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

