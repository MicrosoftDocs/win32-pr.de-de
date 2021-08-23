---
title: IsLSPreventUpgradeGPEnabled-Methode der Win32_TSLicenseServer Klasse
description: Ruft ab, ob \ 0034;Lizenzupgrade verhindern \ 0034; Die Gruppenrichtlinieneinstellung ist auf dem Remotedesktop aktiviert.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- IsLSPreventUpgradeGPEnabled-Remotedesktopdienste
- IsLSPreventUpgradeGPEnabled-Methode Remotedesktopdienste , Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer klasse Remotedesktopdienste , IsLSPreventUpgradeGPEnabled-Methode
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
ms.openlocfilehash: 7958df7d153db0abafd8e463f22a181f2e5a639afa5c21cb7529a9cd5c005c5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511695"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a>IsLSPreventUpgradeGPEnabled-Methode der Win32 \_ TSLicenseServer-Klasse

Ruft ab, ob die Gruppenrichtlinieneinstellung "Lizenzupgrade verhindern" auf dem Remotedesktop aktiviert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Aktiviert* \[ out\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Richtlinieneinstellung "Lizenzupgrade verhindern" aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Wenn die Richtlinieneinstellung "Lizenzupgrade verhindern" aktiviert ist, gibt der Lizenzserver nur dann eine temporäre RDS-CAL an den Client aus, wenn keine geeignete RDS CAL für den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) verfügbar ist.

Die Richtlinieneinstellung befindet sich im folgenden Knoten des Editors für lokale Gruppenrichtlinien:

Computerkonfiguration Administrative Vorlagen \\ \\ \\ Windows-Komponenten Terminaldienste \\ TS-Lizenzierung

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

