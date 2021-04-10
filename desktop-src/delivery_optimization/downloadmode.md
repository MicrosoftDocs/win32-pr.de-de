---
title: Downloadmode-Enumeration (deliveryoptimization. h)
description: Definiert die verschiedenen Download Modi, die von der Übermittlungs Optimierung verwendet werden.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- In diesem Modus wird die Übermittlungsoptimierung umgangen und stattdessen BITS verwendet. Sie können diesen Modus beispielsweise auswählen, damit Clients BranchCache verwenden können. Enumeration
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cde44a3d211040e2cc1dd62afd54f8284f5493e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040526"
---
# <a name="downloadmode-enumeration"></a>Downloadmode-Enumeration

Definiert die verschiedenen Download Modi, die von der Übermittlungs Optimierung verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**
</dt> <dd>

Mit dieser Einstellung wird die Peer-zu-Peer-Zwischenspeicherung deaktiviert, aber dennoch ist es möglich, Inhalte von Microsoft-Servern herunterzuladen. Dieser Modus verwendet zusätzliche Metadaten, die von den Clouddiensten für die Übermittlungs Optimierung bereitgestellt werden, um eine zuverlässige und effiziente Download Leistung zu erzielen.

</dd> <dt>

<span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**
</dt> <dd>

Dieser Standardbetriebsmodus für die Übermittlungsoptimierung aktiviert die Freigabe über Peers im gleichen Netzwerk.

</dd> <dt>

<span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**
</dt> <dd>

Wenn der Gruppenmodus festgelegt ist, wird die Gruppe automatisch basierend auf den Geräten Active Directory Domain Services (AD DS) (Windows 10, Version 1607) oder der Domäne, bei der das Gerät authentifiziert wird, ausgewählt (Windows 10, Version 1511). Im Gruppenmodus erfolgt die Peerfreigabe über interne Subnetze zwischen Geräten, die zur gleichen Gruppe gehören, einschließlich Geräten in Zweigstellen. Sie können die GroupID-Option verwenden, um eine eigene benutzerdefinierte Gruppe zu erstellen, unabhängig von Domänen und AD DS-Sites. Der Downloadmodus „Gruppe“ wird den meisten Organisationen empfohlen, die die beste Bandbreitenoptimierung mit Übermittlungsoptimierung anstreben.

</dd> <dt>

<span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**
</dt> <dd>

Lässt Peerquellen im Internet für die Übermittlungsoptimierung zu.

</dd> <dt>

<span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**
</dt> <dd>

Im Einfachmodus wird die Verwendung von Clouddiensten für die Übermittlungsoptimierung vollständig deaktiviert (für Offlineumgebungen). Die Übermittlungs Optimierung wechselt automatisch in diesen Modus, wenn die Clouddienste für die Übermittlungs Optimierung nicht verfügbar sind, nicht erreichbar sind oder wenn die Größe der Inhalts Datei weniger als 10 MB beträgt. In diesem Modus bietet die Übermittlungs Optimierung einen zuverlässigen Download, ohne Peer-zu-Peer-Caching.

</dd> <dt>

<span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**
</dt> <dd>

In diesem Modus wird die Übermittlungsoptimierung umgangen und stattdessen BITS verwendet. Sie können diesen Modus beispielsweise auswählen, damit Clients BranchCache verwenden können.

</dd> </dl>

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------|----------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>  |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
