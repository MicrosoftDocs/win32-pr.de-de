---
title: DownloadMode-Enumeration (Deliveryoptimization.h)
description: Definiert die verschiedenen Downloadmodi, die Übermittlungsoptimierung verwenden.
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
ms.openlocfilehash: 9ea753ef47dc2e6655d7e707466d7b0448bee7bec1f090b1baf4de04799283d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543724"
---
# <a name="downloadmode-enumeration"></a>DownloadMode-Enumeration

Definiert die verschiedenen Downloadmodi, die Übermittlungsoptimierung verwenden.

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

Diese Einstellung deaktiviert die Peer-zu-Peer-Zwischenspeicherung, ermöglicht Übermittlungsoptimierung das Herunterladen von Inhalten von Microsoft-Servern. In diesem Modus werden zusätzliche Metadaten verwendet, die von Übermittlungsoptimierung Clouddiensten bereitgestellt werden, um eine zuverlässige und effiziente Peerless-Downloaderfahrung zu ermöglichen.

</dd> <dt>

<span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**
</dt> <dd>

Dieser Standardbetriebsmodus für die Übermittlungsoptimierung aktiviert die Freigabe über Peers im gleichen Netzwerk.

</dd> <dt>

<span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**
</dt> <dd>

Wenn der Gruppenmodus festgelegt ist, wird die Gruppe automatisch basierend auf dem Active Directory Domain Services-Standort (AD DS) des Geräts (Windows 10, Version 1607) oder der Domäne ausgewählt, bei der das Gerät authentifiziert wird (Windows 10, Version 1511). Im Gruppenmodus erfolgt die Peerfreigabe über interne Subnetze zwischen Geräten, die zur gleichen Gruppe gehören, einschließlich Geräten in Zweigstellen. Sie können die GroupID-Option verwenden, um eine eigene benutzerdefinierte Gruppe zu erstellen, unabhängig von Domänen und AD DS-Sites. Der Downloadmodus „Gruppe“ wird den meisten Organisationen empfohlen, die die beste Bandbreitenoptimierung mit Übermittlungsoptimierung anstreben.

</dd> <dt>

<span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**
</dt> <dd>

Lässt Peerquellen im Internet für die Übermittlungsoptimierung zu.

</dd> <dt>

<span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**
</dt> <dd>

Im Einfachmodus wird die Verwendung von Clouddiensten für die Übermittlungsoptimierung vollständig deaktiviert (für Offlineumgebungen). Übermittlungsoptimierung automatisch in diesen Modus wechselt, wenn die Übermittlungsoptimierung-Clouddienste nicht verfügbar, nicht erreichbar oder die Größe der Inhaltsdatei kleiner als 10 MB ist. In diesem Modus bietet Übermittlungsoptimierung eine zuverlässige Downloaderfahrung ohne Peer-zu-Peer-Zwischenspeicherung.

</dd> <dt>

<span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**
</dt> <dd>

In diesem Modus wird die Übermittlungsoptimierung umgangen und stattdessen BITS verwendet. Sie können diesen Modus beispielsweise auswählen, damit Clients BranchCache verwenden können.

</dd> </dl>

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------|----------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1709 \[\]<br/>      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>  |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>               |
