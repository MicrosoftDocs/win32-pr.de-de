---
title: Verwenden von NPS-Erweiterungen
description: Der Internet Authentifizierungsdienst (IAS) wurde umbenannt in Netzwerk Richtlinien Server (Network Policy Server, NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Internet Authentifizierungsdienst IAS, Tasks
- Internet Authentication Service IAS, using
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104516682"
---
# <a name="using-nps-extensions"></a>Verwenden von NPS-Erweiterungen

Der Internet Authentifizierungsdienst (IAS) wurde umbenannt in Netzwerk Richtlinien Server (Network Policy Server, NPS). Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

* * Windows Server 2008 R2 und Windows Server 2008: * *

Die Beispiele für Dialin und mapname erweitern die NPS-Funktionalität.



| Beispiel             | BESCHREIBUNG                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dialin<br/>  | In diesem Beispiel wird eine RADIUS-Erweiterungs-DLL implementiert, mit der das einwählbit für den Benutzer überprüft wird.<br/>                                                                                                              |
| Mapname<br/> | Diese Beispiel Erweiterungs-DLL durchsucht alle vertrauenswürdigen Domänen nach dem vorgesehenen Konto. Dadurch können Benutzer aus mehreren Domänen authentifiziert werden, ohne dass die Benutzer ihren Domänen Namen angeben müssen.<br/> |



 

Den Quellcode für die Beispielanwendungen mapname und Dialin finden Sie in der folgenden Liste. *Speicherort*,% Installationspfad%, bestimmt das Basis Installationsverzeichnis für x64-Computer. Weitere Informationen finden Sie unter Windows [Software Development Kit (SDK) für Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK) und [Downloads für die Entwicklung von Windows Store-Apps](https://msdn.microsoft.com/windows/apps/br229516).

<dl> <dt>

Windows SDK für Windows 8
</dt> <dd>

Windows Server 2012

Download Link: N/v

Mapname: Nein

Dialin: Nein

Speicherort: N/v

</dd> <dt>

Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4,0
</dt> <dd>

Windows Server 2008 R2

Download Link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

Mapname: Ja

Dialin: Nein

Speicherort:% Installationspfad% \\ Microsoft sdert \\ Windows \\ v 7.1 \\ Beispiele \\ netds \\ IAS

</dd> <dt>

Windows SDK
</dt> <dd>

Windows Server 2008

Download Link: <https://www.microsoft.com/download/details.aspx?id=5023>

Mapname: Ja

Dialin: Nein

Speicherort:% Installationspfad% \\ Microsoft sdert \\ Windows \\ v 6.1 \\ Beispiele \\ netds \\ IAS

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Downloads für Entwickler](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[Windows SDK für Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





