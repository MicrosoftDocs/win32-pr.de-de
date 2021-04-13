---
title: Win32_RDMSJoinedNode-Klasse
description: Stellt einen Server Knoten dar, der von Remotedesktop Verwaltungsdienste (RDMs) verwaltet wird.
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Win32_RDMSJoinedNode-Klasse Remotedesktopdienste
- Win32_RDMSJoinedNode Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391564"
---
# <a name="win32_rdmsjoinednode-class"></a>Win32 \_ rdmsjoinednode-Klasse

Stellt einen Server Knoten dar, der von Remotedesktop Verwaltungsdienste (RDMs) verwaltet wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdmsjoinednode** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ rdmsjoinednode** -Klasse verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getjoinednoentcount**](win32-rdmsjoinednode-getjoinednodecount.md) | **Windows Server 2012 R2 und Windows Server 2012:** Diese Methode ist vor Windows Server 2016 nicht verfügbar.<br/> Ruft die Anzahl der Server ab, auf denen die angegebene Rolle installiert ist.<br/> |
| [**Join**](join-win32-rdmsjoinednode.md)                             | Fügt RDMs einen Knoten hinzu.<br/>                                                                                                                                                                       |
| [**Entfernen**](unjoin-win32-rdmsjoinednode.md)                         | Entfernt einen Knoten aus RDMs.<br/>                                                                                                                                                                  |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdmsjoinednode** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**FQDN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Ruft den voll qualifizierten Domänen Namen des Knotens ab.

</dd> <dt>

**Isgatewaycertifigateinstemmt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Dient zum Abrufen und Festlegen eines Werts, der angibt, ob der Server über ein Zertifikat zum Durchführen der Authentifizierung für Remotedesktop Gateway-Verbindungen verfügt. **True** , wenn das Zertifikat installiert ist. andernfalls **false**.

</dd> <dt>

**Ispublishingcertifi.**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob der Server über ein Zertifikat zum Signieren Remotedesktopprotokoll Veröffentlichungs Dateien verfügt, oder legt ihn fest. **True** , wenn das Zertifikat installiert ist. andernfalls **false**.

</dd> <dt>

**Isrdcb**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob der Server Remotedesktopverbindung Broker ist, oder legt ihn fest. **True** , wenn es sich bei dem Server um einen Remotedesktopverbindung Broker handelt. andernfalls **false**.

</dd> <dt>

**Isrdg**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob der Server Remotedesktop Gatewayserver ist, oder legt ihn fest. **True** , wenn der Server ein Remotedesktop Gatewayserver ist. andernfalls **false**.

</dd> <dt>

**Isrdls**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob der Server Remotedesktop Lizenzserver ist, oder legt ihn fest. **True** , wenn es sich bei dem Server um einen Remotedesktop Lizenzserver handelt. andernfalls **false**.

</dd> <dt>

**Isrdsh**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob der Server Remotedesktop-Sitzungs Host Servers ist, oder legt ihn fest. **True** , wenn der Server ein Remotedesktop-Sitzungs Host Server ist. andernfalls **false**.

</dd> <dt>

**Isrdvh**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Dient zum Abrufen und Festlegen eines Werts, der angibt, ob der Server Remotedesktop Virtualisierungshost ist. **True** , wenn der Server ein Remotedesktop Virtualisierungshost ist. andernfalls **false**.

</dd> <dt>

**Isrdwa**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob der Server Remotedesktop Web Access-Server ist, oder legt ihn fest. **True** , wenn der Server ein Remotedesktop Webzugriff Server ist. andernfalls **false**.

</dd> <dt>

**Isredirector Certifi.**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Dient zum Abrufen und Festlegen eines Werts, der angibt, ob der Server über ein Zertifikat zum Durchführen der Authentifizierung für Remotedesktopdienste Bereitstellung verfügt. **True** , wenn das Zertifikat installiert ist. andernfalls **false**.

</dd> <dt>

**Iswebaccesscertifierstemmt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob der Server über ein Zertifikat zum Ausführen der Authentifizierung für Remotedesktop Webzugriff verfügt, oder legt ihn fest. **True** , wenn das Zertifikat installiert ist. andernfalls **false**.

</dd> <dt>

**OSVersion**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Ruft die Version der Betriebssysteme auf dem Knoten ab und legt Sie fest.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Ruft die Sicherheits-ID (SID) des Knotens ab.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> </dl>

 

