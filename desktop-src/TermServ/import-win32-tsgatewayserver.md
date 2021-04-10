---
title: Import-Methode der Win32_TSGatewayServer-Klasse
description: Importiert eine angegebene Konfiguration auf den Remotedesktop Gateway-Server (RD-Gateway).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Import Methode Remotedesktopdienste
- Import-Methode Remotedesktopdienste, Win32_TSGatewayServer-Klasse
- Win32_TSGatewayServer-Klasse Remotedesktopdienste, Import-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956678"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Import-Methode der Win32-Klasse "t- \_ Gatewayserver"

Importiert eine angegebene Konfiguration auf den Remotedesktop Gateway-Server (RD-Gateway).

## <a name="syntax"></a>Syntax


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Importtype* \[ in\]
</dt> <dd>

Der zu importierende Inhalt. Legen Sie den Importtyp fest, indem Sie die entsprechenden Bits im *importttype* -Parameter festlegen. Sie können mehrere Import Typen festlegen. Wenn z. b. das 0-Bit festgelegt ist, werden Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD-CAPs) importiert. Wenn sowohl das 0 als auch das zweite Bit festgelegt ist, werden sowohl RD-CAPs als auch Remotedesktopdienste Ressourcen Autorisierungs Richtlinien (RD-RAPs) importiert.

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Alle Caps importieren** (1)


</dt> <dd>

Importieren Sie alle RD-Caps.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Alle RADIUS-Server importieren** (2)


</dt> <dd>

Importieren Sie eine Liste aller Netzwerk Richtlinien Server-Server (NPS).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Alle Raps importieren** (4)


</dt> <dd>

Importieren Sie alle RD-RAPs.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Alle RGS importieren** (8)


</dt> <dd>

Importieren Sie alle Ressourcengruppen.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Alle Loadbalancing-Server importieren** (16)


</dt> <dd>

Importieren Sie eine Liste aller Lasten Ausgleichs Server.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Alle Server Einstellungen importieren** (32)


</dt> <dd>

Importieren Sie alle RD-Gateway bezogenen Servereinstellungen.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Alle Integritäts Richtlinien importieren** (64)


</dt> <dd>

Importieren Sie alle Integritäts Richtlinien.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008: * *

Dieser Wert wird vor Windows Server 2016 nicht unterstützt.

</dd> </dl> </dd> <dt>

*XmlString* \[ in\]
</dt> <dd>

Die Konfiguration als XML-Zeichenfolge.

</dd> <dt>

*Mergeorreplace* \[ in\]
</dt> <dd>

Gibt an, ob Daten zusammengeführt oder ersetzt werden sollen, wenn ein Konflikt auftritt.

> [!Note]  
> Merge ist noch nicht implementiert. Daher wird dieser Parameterwert ignoriert.

 

</dd> <dt>

*Logstring* \[ vorgenommen\]
</dt> <dd>

Die Protokollinformationen, die während des Import Vorgangs generiert werden.

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

 

