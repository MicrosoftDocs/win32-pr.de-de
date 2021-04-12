---
title: Islssecgrpgpabled-Methode der Win32_TSLicenseServer-Klasse
description: Ruft ab, ob die Sicherheitsgruppe \ 0034; Lizenzserver \ 0034; die Gruppenrichtlinien Einstellung ist auf dem Remotedesktop-Lizenzserver aktiviert.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Islssecgrpgpabled-Methode Remotedesktopdienste
- Islssecgrpgpabled-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, islssecgrpgpabled-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104301"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a>Islssecgrpgpabled-Methode der Win32- \_ Klasse "zlicenseserver"

Ruft ab, ob die Gruppenrichtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" auf dem Remotedesktop-Lizenzserver aktiviert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Aktiviert* \[ vorgenommen\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Richtlinien Einstellung für die Sicherheitsgruppe "Lizenzserver" aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Mit der Richtlinien Einstellung "Lizenzserver-Sicherheitsgruppe" können Sie die Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server angeben, die zum Abrufen von Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) mit dem Lizenzserver berechtigt sind. Wenn die Richtlinien Einstellung auf dem Lizenzserver aktiviert ist, antwortet der Server nur auf RDS-Anforderungen von RD-Sitzungshost Servern, deren Computer Konten Mitglied der lokalen Gruppe "Terminal Server Computer" auf dem Lizenzserver sind.

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

 

