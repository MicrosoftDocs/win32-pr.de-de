---
description: Entfernen von UDDI-Diensten aus dem Serverbetriebssystem
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Entfernen von UDDI-Diensten aus dem Serverbetriebssystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530c6aadbe4e1dce32f3cc2e212af823eb565b85b67c5f7f29b77015f75bc899
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328999"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Entfernen von UDDI-Diensten aus dem Serverbetriebssystem

## <a name="affected-platform"></a>Betroffene Plattform

**Server** – Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkung von Features

**Schweregrad:** Mittel  
**Häufigkeit** – Niedrig  

## <a name="description"></a>BESCHREIBUNG

Microsoft hat die Serverrolle UDDI (Universal Description, Discovery, and Integration) Services aus Windows Server 2008 R2 entfernt. Zukünftige Releases von UDDI Services werden Teil des Microsoft BizTalk-Produkts sein. Diese Produktentwicklung und Konsolidierung positioniert Microsoft, um den Markt für die dienstorientierte Architektur (SoA) besser bedienen zu können.

Die erste Version Windows Server 2008 von UDDI Services ist mit UDDI v3.0-Standards kompatibel. Es wird als Teil des Release BizTalk Server 2009 veröffentlicht. Um unsere Verpflichtung zur Bereitstellung einer zufriedenstellenden Benutzererfahrung zu erfüllen, bieten wir ein Installationspaket für UDDI Services v3 für Windows Server 2008 R2 an.

## <a name="manifestation"></a>Manifestation

Das Vorhandensein vorheriger Versionen von UDDI Services-Komponenten auf dem System blockiert ein Upgrade auf Windows Server 2008 R2.

## <a name="mitigation-of-impact"></a>Entschärfung der Auswirkungen

Benutzer, die einen UDDI Services-Standort von Windows Server 2003 oder Windows Server 2008 bereitgestellt haben, können die Server, auf denen die UDDI-Dienste ausgeführt werden, nicht auf Windows Server 2008 R2 aktualisieren. Sie können die UDDI-Dienste auch in dedizierte Windows Server 2003- oder Windows Server 2008-Felder verschieben, wenn sie die aktuellen FELDER für UDDI-Dienste aktualisieren müssen.

## <a name="solution"></a>Lösung

Die empfohlene Lösung besteht in der Bereitstellung von UDDI Services v3.0 von BizTalk Server 2009 auf einem Windows Server 2008 R2-Computer und anschließendes Migrieren des alten Standorts zum neuen Standort. UDDI Services v3.0 bietet Abwärtskompatibilität mit UDDI Services 2.0, sodass alle Anwendungen, die UDDI-Dienste verwenden, davon nicht betroffen sind.

Gehen Sie hierzu folgendermaßen vor:

1.  Richten Sie einen neuen UDDI Services v3.0-Standort auf einem Computer ein, der bereits mit Windows Server 2008 R2 geladen wurde. (Hinweis: In einem verteilten Setup kann ein UDDI v3.0-Standort aus mehr als einem Windows Server 2008 R2-Computer bestehen.)
2.  Verwenden Sie das UDDI-Datenmigrationstool, um die Daten aus der alten UDDI Services-Datenbank zur neuen Datenbank zu migrieren.
3.  Sichern Sie die alte UDDI Services-Datenbank, um die Rollbackfunktion sicherzustellen.
4.  Deinstallieren Sie die alte UDDI Services-Software, und aktualisieren Sie diese Felder auf Windows Server 2008 R2.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Microsoft UDDI Services-Website](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [UDDI-Spezifikationen](http://uddi.xml.org/specification)
-   [UdDI Services v3.0-Download für Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



