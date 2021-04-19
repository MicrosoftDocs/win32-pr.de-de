---
description: .
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Entfernen der UDDI-Dienste aus dem Server Betriebssystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7681167177b850ba44ac0fc26e019c7393008b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353930"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a>Entfernen der UDDI-Dienste aus dem Server Betriebssystem

## <a name="affected-platform"></a>Betroffene Plattform

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -Mittel  
**Häufigkeit** -niedrig  

## <a name="description"></a>BESCHREIBUNG

Die UDDI-Server Rolle (universelle Beschreibung, Ermittlung und Integration) von Windows Server 2008 R2 wurde von Microsoft entfernt. Zukünftige Versionen der UDDI-Dienste sind Teil des Microsoft BizTalk-Produkts. Durch die Neuausrichtung und Konsolidierung von Produkten wird Microsoft zur Verbesserung der Dienst orientierten Architektur (Service-Oriented Architecture, SOA).

Die erste Version nach Windows Server 2008 der UDDI-Dienste wird mit UDDI v 3.0-Standards kompatibel sein. Sie wird als Teil der Version BizTalk Server 2009 ausgeliefert. Um unsere Verpflichtung zu erfüllen, eine zufriedenstellende Benutzerfunktion bereitzustellen, bieten wir ein UDDI Services V3-Installationspaket für Windows Server 2008 R2.

## <a name="manifestation"></a>Ausstrahlung

Wenn frühere Versionen der UDDI-Dienstekomponenten auf dem System vorhanden sind, wird ein Upgrade auf Windows Server 2008 R2 blockiert.

## <a name="mitigation-of-impact"></a>Minderung der Auswirkung

Benutzer, die eine UDDI-Dienst Website von Windows Server 2003 oder Windows Server 2008 bereitgestellt haben, können die Server, auf denen die UDDI-Dienste ausgeführt werden, nicht auf Windows Server 2008 R2 aktualisieren. Sie können die UDDI-Dienste auch in dedizierte Windows Server 2003-oder Windows Server 2008-Felder verschieben, wenn Sie die aktuellen UDDI-Dienst Felder aktualisieren müssen.

## <a name="solution"></a>Lösung

Die empfohlene Lösung besteht darin, die UDDI-Dienste v 3.0 von BizTalk Server 2009 auf einem Windows Server 2008 R2-Computer bereitzustellen und dann den alten Standort zum neuen Standort zu migrieren. UDDI Services v 3.0 bietet Abwärtskompatibilität mit den UDDI-Diensten 2,0, sodass alle Anwendungen, die UDDI-Dienste verwenden, nicht betroffen sind.

Gehen Sie hierzu folgendermaßen vor:

1.  Richten Sie eine neue UDDI-Dienste v 3.0-Website auf einem Computer ein, der bereits mit Windows Server 2008 R2 geladen wurde. (Hinweis: in einem verteilten Setup kann ein UDDI v 3.0-Standort aus mehr als einem Windows Server 2008 R2-Computer bestehen.)
2.  Verwenden Sie das Daten Migrationstool von UDDI zum Migrieren der Daten aus der alten Datenbank der UDDI-Dienste in die neue Datenbank.
3.  Sichern Sie die alte Datenbank der UDDI-Dienste, um die Rollback-Funktion sicherzustellen.
4.  Deinstallieren Sie die alte UDDI-Dienst Software, und führen Sie ein Upgrade dieser Felder auf Windows Server 2008 R2 aus.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Website für Microsoft UDDI-Dienste](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [UDDI-Spezifikationen](http://uddi.xml.org/specification)
-   [Download der UDDI-Dienste v 3.0 für Windows Server 2008 R2](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



