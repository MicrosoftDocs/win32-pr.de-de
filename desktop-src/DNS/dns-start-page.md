---
title: Domain Name System (DNS)
description: Domain Name System (DNS), ein Serverlocatorpunkt-Dienst in Microsoft Windows, ist ein Industriestandard Protokoll, mit dem Computer in einem IP-basierten Netzwerk lokalisiert werden.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS (siehe Domain Name System)
- Domain Name System (DNS)
- Domain Name System, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104050826"
---
# <a name="domain-name-system"></a>Domain Name System (DNS)

## <a name="purpose"></a>Zweck

Domain Name System (DNS), ein Serverlocatorpunkt-Dienst in Microsoft Windows, ist ein Industriestandard Protokoll, mit dem Computer in einem IP-basierten Netzwerk lokalisiert werden. IP-Netzwerke, wie z. b. das Internet und Windows-Netzwerke, basieren auf Zahlen basierten Adressen, um Daten zu verarbeiten. Benutzer können sich jedoch leichter mit Namen Adressen merken, sodass benutzerfreundliche Namen (z. b.) in Adressen übersetzt werden müssen, `www.microsoft.com` die das Netzwerk erkennen kann (z. b. 207.46.131.137).

## <a name="where-applicable"></a>Anwendungsbereich

In Windows und Active Directory wird DNS verwendet. DNS ist der primäre Serverlocatorpunkt-Dienst für das Internet und Active Directory. Daher wird DNS als Basis Dienst für Windows und Active Directory angesehen.

## <a name="developer-audience"></a>Entwicklergruppe

Windows stellt Funktionen bereit, mit denen Anwendungsprogrammierer DNS verwenden können, wie z. b. programmgesteuerte DNS-Abfragen, Daten Satz Vergleiche und Namenssuche.

Programmierbare DNS-Komponenten sind für die Verwendung durch C/C++-Programmierer konzipiert. Vertrautheit mit Netzwerk und DNS ist erforderlich. Programmierer sollten mit der IP-Protokoll Suite sowie mit dem DNS-Protokoll und den DNS-Vorgängen vertraut sein.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

DNS wird in allen IP-Netzwerken verwendet, für die ein Internet kompatibler Serverlocatorpunkt-Dienst erforderlich ist. Allerdings erfordert die DNS-API Windows 2000 oder höher.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                             | BESCHREIBUNG                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [DNS-Standarddokumente](dns-standards-documents.md)<br/> | Links zu öffentlichen DNS-Standarddokumenten.<br/>                                  |
| [Informationen zu DNS](about-dns.md)<br/>                             | Allgemeine Informationen zu DNS.<br/>                                            |
| [DNS-Verweis](dns-reference.md)<br/>                     | Referenz Dokumentation für DNS.<br/>                                          |
| [DNS-WMI-Anbieter](dns-wmi-provider.md)<br/>               | Allgemeine Informationen und Referenz Dokumentation für den DNS-WMI-Anbieter.<br/> |
| [Glossar](glossary-gly.md)<br/>                           | Glossar der DNS-Begriffe und-Definitionen.<br/>                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DHCP](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Internet Protokoll-Hilfsprogramm](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

[Verzeichnisdienste](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)
</dt> </dl>

 

