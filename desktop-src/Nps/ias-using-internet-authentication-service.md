---
title: Verwenden von NPS-Erweiterungen
description: Erfahren Sie mehr über die Verwendung von NPS-Erweiterungen. Internet Authentication Service (IAS) wurde in Network Policy Server (NPS) umbenannt.
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Internet Authentication Service IAS , Tasks
- Internetauthentifizierungsdienst IAS mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3590ed10ec77e57c86bfad3e0e0b1160e70a2d6fcc08abc911a14614543f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074300"
---
# <a name="using-nps-extensions"></a>Verwenden von NPS-Erweiterungen

Internet Authentication Service (IAS) wurde in Network Policy Server (NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

**Windows Server 2008 R2 und Windows Server 2008: **

Die Beispiele DialIn und MapName erweitern die NPS-Funktionalität.



| Beispiel             | BESCHREIBUNG                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dialin<br/>  | In diesem Beispiel wird eine RADIUS-Erweiterungs-DLL implementiert, die das Einwählbit für den Benutzer überprüft.<br/>                                                                                                              |
| MapName<br/> | Diese Beispielerweiterungs-DLL durchsucht alle vertrauenswürdigen Domänen nach dem angegebenen Konto. Dadurch können Benutzer aus mehreren Domänen authentifiziert werden, ohne dass die Benutzer ihren Domänennamen angeben müssen.<br/> |



 

Den Quellcode für die MapName- und DialIn-Beispielanwendungen finden Sie in der folgenden Liste. *Speicherort*, %Installationspfad%, bestimmt das Basisinstallationsverzeichnis für x64-Computer. Siehe [auch Windows Software Development Kit (SDK) für Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK) und [Downloads für Windows Store App-Entwicklung.](https://msdn.microsoft.com/windows/apps/br229516)

<dl> <dt>

Windows SDK für Windows 8
</dt> <dd>

Windows Server 2012

Downloadlink: N/A

MapName: Nein

DialIn: Nein

Standort: N/A

</dd> <dt>

Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4.0
</dt> <dd>

Windows Server 2008 R2

Downloadlink: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

MapName: Ja

DialIn: Nein

Speicherort: %Install Path% \\ Microsoft SDKs \\ Windows \\ v7.1 \\ Samples \\ netds \\ ias

</dd> <dt>

Windows SDK
</dt> <dd>

Windows Server 2008

Downloadlink: <https://www.microsoft.com/download/details.aspx?id=5023>

MapName: Ja

DialIn: Nein

Speicherort: %Installationspfad% \\ Microsoft SDKs \\ Windows \\ v6.1 \\ Samples \\ NetDs \\ IAS

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Downloads für Entwickler](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[Windows SDK für Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





