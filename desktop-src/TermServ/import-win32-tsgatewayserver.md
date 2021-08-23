---
title: Import-Methode der Win32_TSGatewayServer-Klasse
description: Importiert eine bestimmte Konfiguration auf den Server des Remotedesktop-Gateways (RD-Gateway).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Importmethode
- Importmethode Remotedesktopdienste , Win32_TSGatewayServer-Klasse
- Win32_TSGatewayServer-Klasse Remotedesktopdienste , Import-Methode
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
ms.openlocfilehash: 2629e8e44acd0f617e86a846cc127ab77250673c8612f2d2f53ab8c0238d9f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574570"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Import-Methode der Win32 \_ TSGatewayServer-Klasse

Importiert eine bestimmte Konfiguration auf den Server des Remotedesktop-Gateways (RD-Gateway).

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

*ImportType* \[ In\]
</dt> <dd>

Der zu importierende Inhalt. Legen Sie den Importtyp fest, indem Sie die entsprechenden Bits im *ImportType-Parameter* festlegen. Sie können mehrere Importtypen festlegen. Wenn z. B. 0 Bit festgelegt ist, werden Remotedesktopdienste Verbindungsautorisierungsrichtlinien (RD CAPs) importiert. Wenn sowohl das 0- als auch das 2. Bit festgelegt ist, werden sowohl RD-CAPs als auch Remotedesktopdienste Ressourcenautorisierungsrichtlinien (RESOURCE Authorization Policies, RD RAPs) importiert.

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importieren aller CAPs** (1)


</dt> <dd>

Importieren Sie alle RD-CAPs.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importieren aller Radius-Server** (2)


</dt> <dd>

Importieren Sie eine Liste aller NPS-Server (Network Policy Server).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importieren aller RAPs** (4)


</dt> <dd>

Importieren Sie alle RD-RAPs.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importieren aller RGs** (8)


</dt> <dd>

Importieren Sie alle Ressourcengruppen.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importieren aller LoadBalancing-Server** (16)


</dt> <dd>

Importieren Sie eine Liste aller Lastenausgleichsserver.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importieren aller Server-Einstellungen** (32)


</dt> <dd>

Importieren Sie alle RD-Gateway-bezogenen Servereinstellungen.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importieren aller Integritätsrichtlinien** (64)


</dt> <dd>

Importieren Sie alle Integritätsrichtlinien.

**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 und Windows Server 2008: **

Dieser Wert wird vor Windows Server 2016 nicht unterstützt.

</dd> </dl> </dd> <dt>

*XmlString* \[ In\]
</dt> <dd>

Die Konfiguration als XML-Zeichenfolge.

</dd> <dt>

*MergeOrReplace* \[ In\]
</dt> <dd>

Gibt an, ob Daten zusammengeführt oder ersetzt werden sollen, wenn ein Konflikt auftritt.

> [!Note]  
> Merge ist noch nicht implementiert. Daher wird dieser Parameterwert ignoriert.

 

</dd> <dt>

*LogString* \[ out\]
</dt> <dd>

Die Protokollinformationen, die während des Importvorgangs generiert werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSGatewayServer**](win32-tsgatewayserver.md)
</dt> </dl>

 

