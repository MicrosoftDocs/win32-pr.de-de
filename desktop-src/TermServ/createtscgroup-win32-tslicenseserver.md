---
title: Die Methode "kreatetscgroup" der Win32_TSLicenseServer-Klasse
description: "\"\" Ist für Windows Server 2012 nicht mehr verfügbar."
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "kreatetscgroup"
- Methode Remotedesktopdienste der Methode "kreatetscgroup", Win32_TSLicenseServer
- Win32_TSLicenseServer Klasse Remotedesktopdienste, Methode "kreatetscgroup"
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f10db61cb02ece09d168cb462e31246e498494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858720"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a>Methode "foratetscgroup" der Win32- \_ Klasse "zlicenseserver"

\[" **" Ist für** Windows Server 2012 nicht mehr verfügbar.\]

Diese Methode wird nicht unterstützt.

**Windows Server 2008 R2 und Windows Server 2008:** Erstellt die lokale Gruppe "Terminal Server Computer" auf dem Remotedesktop-Lizenz Server.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **WBEM \_ E \_ nicht \_ unterstützt** zurück.

**Windows Server 2008 R2 und Windows Server 2008:** Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                                 |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                         |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Lizenznehmer**](win32-tslicenseserver.md)
</dt> <dt>

[**Istscgrouppresent**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

