---
title: Spezifikation für die Benutzeroberflächenautomatisierung und Zusicherung an die Community
description: Die Benutzeroberflächenautomatisierung-Spezifikation enthält Informationen zu Microsoft-Frameworks für die Barrierefreiheit, einschließlich Microsoft Active Accessibility und Microsoft Benutzeroberflächenautomatisierung.
ms.assetid: 5fab2d7a-0b1c-4119-b7f4-afdf86db74e7
keywords:
- Benutzeroberflächenautomatisierung, Spezifikationen
- Benutzeroberflächenautomatisierung, Community-Zusage
- Spezifikationen für Benutzeroberflächenautomatisierung
- Communityversprechen für Benutzeroberflächenautomatisierung
- Benutzeroberflächenautomatisierung, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9a71b5946f7e0b38241a1d7ef7ced9832203bfd4f0637032903f4dad948607
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570490"
---
# <a name="ui-automation-specification-and-community-promise"></a>Spezifikation für die Benutzeroberflächenautomatisierung und Zusicherung an die Community

Die Benutzeroberflächenautomatisierung-Spezifikation enthält Informationen zu Microsoft-Frameworks für die Barrierefreiheit, einschließlich Microsoft Active Accessibility und Microsoft Benutzeroberflächenautomatisierung. Es werden die Hauptkomponenten der einzelnen Frameworks erläutert, Entwurfsüberlegungen und -beispiele sowie Anforderungen für die Implementierung beschrieben. Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung-Spezifikation.](ui-automation-specification.md)

Die Benutzeroberflächenautomatisierung Community Promise ermöglicht es jedem, die Benutzeroberflächenautomatisierung-Spezifikation frei zu implementieren, ohne Vereinbarungen mit Microsoft unterzeichnen zu müssen. Darüber hinaus ist es nicht erforderlich, Microsoft zu erwähnen oder darauf zu verweisen. Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung Community Promise](uiauto-specandcommunitypromise.md).

## <a name="ui-automation-specification"></a>Benutzeroberflächenautomatisierung-Spezifikation

Die Benutzeroberflächenautomatisierung-Spezifikation enthält Informationen zu den Barrierefreiheitsframeworks von Microsoft, einschließlich Active Accessibility, Benutzeroberflächenautomatisierung und Benutzeroberflächenautomatisierung Express. Es werden die Hauptkomponenten der einzelnen Frameworks erläutert, Entwurfsüberlegungen und -beispiele sowie Anforderungen für die Implementierung beschrieben.

### <a name="ui-automation-specification-copyright-license"></a>copyright-Lizenz für Benutzeroberflächenautomatisierung-Spezifikation

Die folgende Urheberrechtslizenz gilt für die Benutzeroberflächenautomatisierung-Spezifikation und muss in allen Kopien der Benutzeroberflächenautomatisierung-Spezifikation enthalten sein. Die aktuelle Benutzeroberflächenautomatisierung-Spezifikation ist im Microsoft Download Center verfügbar.

### <a name="legal-notice"></a>Rechtliche Hinweise

Die Berechtigung zum Kopieren, Anzeigen und Verteilen des Inhalts dieses Dokuments (der "Spezifikation") auf einem beliebigen Medium für beliebige Zwecke ohne Gebühr oder Lizenzgebühren wird gewährt, vorausgesetzt, Sie fügen den folgenden Hinweis auf ALLE Kopien der Spezifikation oder Teile davon ein, die Sie vornehmen:

Copyright © Microsoft Corporation. All rights reserved. Die Berechtigung zum Kopieren, Anzeigen und Verteilen dieses Dokuments ist unter [Benutzeroberflächenautomatisierung Community Promise](uiauto-specandcommunitypromise.md)verfügbar.

Sie können abgeleitete Arbeiten der Spezifikation erstellen, vorausgesetzt, Sie schließen alle erforderlichen Teile der Spezifikation in Ihre Ableitungsarbeit ein und stellen den obigen Hinweis bereit.

Es gibt ein separates Patentversprechen für Parteien, die an der Implementierung von Software interessiert sind, die der Benutzeroberflächenautomatisierung-Spezifikation entspricht. Diese Patentlizenz ist an diesem Speicherort verfügbar: [Benutzeroberflächenautomatisierung Community Promise](uiauto-specandcommunitypromise.md)

Die Spezifikation wird "wie benutzbar" bereitgestellt, und Microsoft übernimmt keine ausdrücklichen oder konkludenten Zusicherungen oder Gewährleistungen, einschließlich, aber nicht beschränkt auf Gewährleistungen der Handelsüblichkeit, Eignung für einen bestimmten Zweck, Nichtverletzung oder Titel; , dass der Inhalt der Spezifikation für jeden Zweck geeignet ist; und dass die Implementierung solcher Inhalte keine Drittanbieterrechte, Copyrights, Marken oder andere Rechte verletzt. Microsoft ist nicht für direkte, indirekte, spezielle, zufällige oder Folgeschäden verantwortlich, die sich aus oder im Zusammenhang mit der Nutzung oder Verteilung der Spezifikation ergeben.

Der Name und die Marken von Microsoft dürfen NICHT in irgendeiner Weise verwendet werden, einschließlich Werbung oder Werbung im Zusammenhang mit der Spezifikation oder ihren Inhalten ohne spezifische, schriftliche vorherige Genehmigung. Der Titel des Copyrights in der Spezifikation verbleibt jederzeit bei Microsoft.

Es werden keine weiteren Rechte gewährt, weder stillschweigend noch durch Präklusion oder anderweitig.

## <a name="ui-automation-community-promise"></a>Benutzeroberflächenautomatisierung Community Promise

Microsoft verpflichtet sich, keine von Microsoft erforderlichen Ansprüche gegen Sie für das Erstellen, Verwenden, Verkaufen, Anbieten zum Verkauf, Importieren oder Verteilen von Implementierungen zu bestätigen, sofern sie einer der abgedeckten Spezifikationen entsprechen und mit allen erforderlichen Teilen der obligatorischen Bestimmungen dieser Spezifikation ("Abgedeckte Implementierung") konform sind, sofern folgende Bedingungen erfüllt sind:

Dies ist eine persönliche Zusage direkt von Microsoft an Sie, und Sie bestätigen, dass Sie davon profitieren, dass keine Microsoft-Rechte von Lieferanten, Verteilern oder anderweitig im Zusammenhang mit dieser Zusage erhalten werden. Wenn Sie eine Microsoft-Implementierung einer abgedeckten Spezifikation einreichen, verwalten oder sich freiwillig an einer Patentverletzungsverletzung beteiligen, gilt diese persönliche Zusage nicht in Bezug auf die von Ihnen vorgenommene oder verwendete abgedeckte Implementierung. Zur Verdeutlichung sind "Erforderliche Microsoft-Ansprüche" die Ansprüche von Microsoft-eigenen oder von Microsoft kontrollierten Patenten, die erforderlich sind, um die erforderlichen Teile (die auch die erforderlichen Elemente optionaler Teile enthalten) der abgedeckten Spezifikation zu implementieren, die im Detail beschrieben werden, und nicht diejenigen, auf die lediglich in der abgedeckten Spezifikation verwiesen wird.

Diese Zusage von Microsoft stellt keine Zusicherung dar, dass entweder (i) eines der ausgestellten Patentansprüche von Microsoft eine abgedeckte Implementierung abdeckt oder erzwungen werden kann oder (ii) eine abgedeckte Implementierung keine Verletzungen von Ansprüchen oder anderen Rechten an geistigem Eigentum dritter Personen darstellen würde. Außer den in dieser Zusage ausdrücklich genannten Rechten gelten keine anderen Rechte als gewährt, aufgehoben oder durch Implizite, Erschöpfung, Verpuffung oder sonstiges empfangen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Grundlagen der Benutzeroberflächenautomatisierung](entry-uiautocore-overview.md)
</dt> </dl>

 

 




