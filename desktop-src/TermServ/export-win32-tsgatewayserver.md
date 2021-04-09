---
title: Export-Methode der Win32_TSGatewayServer-Klasse
description: Gibt die Serverkonfiguration des Remotedesktop Gateway (RD-Gateway) als XML-Zeichenfolge zurück.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Export Methode Remotedesktopdienste
- Export Methode Remotedesktopdienste, Win32_TSGatewayServer Klasse
- Win32_TSGatewayServer-Klasse Remotedesktopdienste, Export-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957230"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a>Export-Methode der Win32-Klasse "t- \_ Gatewayserver"

Gibt die Serverkonfiguration des Remotedesktop Gateway (RD-Gateway) als XML-Zeichenfolge zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ExportType* \[ in\]
</dt> <dd>

Der zu exportier-Inhalt. Legen Sie den Exporttyp fest, indem Sie die entsprechenden Bits im *ExportType* -Parameter festlegen. Sie können mehrere Export Typen festlegen. Wenn z. b. das 0-Bit festgelegt ist, werden Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD-CAPs) exportiert. Wenn sowohl das 0 als auch das zweite Bit festgelegt ist, werden sowohl RD-CAPs als auch Remotedesktopdienste Ressourcen Autorisierungs Richtlinien (RD-RAPs) exportiert.

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Alle Caps exportieren** (1)


</dt> <dd>

Exportieren Sie alle RD-Caps.

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Alle RADIUS-Server exportieren** (2)


</dt> <dd>

Exportieren Sie eine Liste aller Netzwerk Richtlinien Server-Server (NPS).

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Alle Raps exportieren** (4)


</dt> <dd>

Exportieren Sie alle RD-RAPs.

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Alle RGS exportieren** (8)


</dt> <dd>

Exportieren aller Ressourcengruppen

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Alle Loadbalancing-Server exportieren** (16)


</dt> <dd>

Exportieren Sie eine Liste aller Lasten Ausgleichs Server.

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Alle Server Einstellungen exportieren** (32)


</dt> <dd>

Exportieren Sie alle RD-Gateway bezogenen Servereinstellungen.

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Alle Integritäts Richtlinien exportieren** (64)


</dt> <dd>

Exportieren Sie alle Integritäts Richtlinien.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008: * *

Dieser Wert wird vor Windows Server 2016 nicht unterstützt.

</dd> </dl> </dd> <dt>

*XmlString* \[ vorgenommen\]
</dt> <dd>

Die XML-Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>"T-Gateway. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Gatewayserver**](win32-tsgatewayserver.md)
</dt> </dl>

 

