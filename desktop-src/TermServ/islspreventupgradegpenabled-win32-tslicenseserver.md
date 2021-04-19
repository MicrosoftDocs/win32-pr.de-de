---
title: Isllexventupgradegpabled-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob das \ 0034-Lizenz Upgrade verhindert wird \ 0034; die Gruppenrichtlinien Einstellung ist auf dem Remotedesktop-Lizenzserver aktiviert.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Die Methode "islspventupgradegpabled" Remotedesktopdienste
- Remotedesktopdienste der Methode "islspventupgradegpabled", Win32_TSLicenseServer Klasse
- Win32_TSLicenseServer Klasse Remotedesktopdienste, die Methode "islspventupgradegpabled"
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345304"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a>Isllexventupgradegpabled-Methode der Win32- \_ Klasse "zlicenseserver"

Ruft ab, ob die Gruppenrichtlinien Einstellung "Lizenz Upgrade verhindern" auf dem Remotedesktop-Lizenzserver aktiviert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Aktiviert* \[ vorgenommen\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Richtlinien Einstellung "Lizenz Upgrade verhindern" aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Wenn die Richtlinien Einstellung "Lizenz Upgrade verhindern" aktiviert ist, stellt der Lizenzserver nur eine temporäre RDS-Client Zugriffslizenz für den Client aus, wenn keine entsprechende RDS-CAL für den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) verfügbar ist.

Die Richtlinien Einstellung befindet sich im folgenden Knoten des Editors für lokale Gruppenrichtlinien:

Computer Konfiguration \\ Administrative Vorlagen \\ \\ terminaldiensteterminaldienstelizenzierung von Windows-Komponenten \\

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Lizenznehmer**](win32-tslicenseserver.md)
</dt> </dl>

 

