---
description: Die icertview-Schnittstelle wird von ordnungsgemäß autorisierten Clients verwendet, um die Zertifikat Dienst Datenbank anzuzeigen.
ms.assetid: c8f316dd-186b-4e4a-b0ce-561a23b266cb
title: Anzeigen der Zertifikat Dienst Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c553cee2f64c3096e733d588c9e0ad3d08ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131724"
---
# <a name="viewing-the-certificate-services-database"></a>Anzeigen der Zertifikat Dienst Datenbank

Die [**icertview**](/windows/desktop/api/Certview/nn-certview-icertview) -Schnittstelle wird von ordnungsgemäß autorisierten Clients verwendet, um die Zertifikat Dienst Datenbank anzuzeigen. Beachten Sie, dass das MMC-Snap-in "Zertifizierungsstelle" im Rahmen des gelieferten Produkts zum Anzeigen der Zertifikat Dienst Datenbank verwendet werden kann. [**Icertview**](/windows/desktop/api/Certview/nn-certview-icertview) wird zum programmgesteuerten Anzeigen der Datenbank bereitgestellt. Die Unterstützung für die **icertview** -Schnittstelle beginnt mit Windows XP.

Bei einem ordnungsgemäß autorisierten Client handelt es sich um einen Benutzer, dem die Berechtigung zum Anzeigen der Zertifikat Dienst Datenbank gewährt wurde. das MMC-Snap-in "Zertifizierungsstelle" kann verwendet werden, um den Zugriff zum Anzeigen der Datenbank zu gewähren oder einzuschränken (Klicken Sie unter **Eigenschaften** für die [*Zertifizierungs*](../secgloss/c-gly.md)Stelle auf die Registerkarte **Sicherheit** ). Um das [**icertview**](/windows/desktop/api/Certview/nn-certview-icertview) -Objekt verwenden zu können, muss die Client Arbeitsstation zusätzlich die Client Komponenten der Zertifikat Dienste installiert haben.

Obwohl es verschiedene Szenarios für die Verwendung von [**icertview**](/windows/desktop/api/Certview/nn-certview-icertview) und der zugehörigen Schnittstellen gibt, stellt das folgende eine mögliche Sequenz zum Entwickeln einer Client Anwendung auf der Grundlage von **icertview** dar:

**So zeigen Sie die Zertifikat Dienst Datenbank an**

1.  Nachdem Sie eine Instanz des [**icertview**](/windows/desktop/api/Certview/nn-certview-icertview) -Objekts erhalten haben, müssen Sie [**icertview:: OpenConnection**](/windows/desktop/api/Certview/nf-certview-icertview-openconnection) aufrufen, um mit einer [*Zertifizierungs*](../secgloss/c-gly.md) Stelle auf einem bestimmten Computer zu kommunizieren.
2.  Nennen Sie [**icertview:: settresultcolumncount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) , um die Anzahl der Spalten in der Sicht anzugeben. Dieser Befehl wird auch verwendet, um eine Standardansicht anzugeben. Wenn im Aufruf keine Standardansicht angegeben ist, muss der Aufrufer für jede Spalte, die in der Sicht enthalten sein soll, [**icertview:: abtresultcolumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn) aufgerufen werden.
3.  Dies ist optional. Geben Sie Sortierkriterien und/oder qualifizierende Kriterien für die Datenbankabfrage an, indem Sie die [**icertview:: abtrestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) -Funktion aufrufen. Bei den qualifizierenden Kriterien wird die Ansicht zum Abrufen von Daten auf der Grundlage von Qualifizierern wie "größer als", "kleiner als", "gleich" usw. angezeigt.
4.  Rufen Sie [**icertview:: OpenView**](/windows/desktop/api/Certview/nf-certview-icertview-openview) auf, um die Daten in der Ansicht abzurufen. die Daten der Ansicht bestehen aus den Spalten, die mithilfe von [**icertview:: settresultcolumncount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) angefordert werden (und wenn keine Standardansicht angegeben wurde, [**icertview:: abtresultcolumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn)). Wenn [**icertview:: abtrestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) aufgerufen wurde, werden die Daten in den Spalten sortiert und/oder qualifiziert. **Icertview:: OpenView** erstellt ein [**ienumcertviewrow**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) -Objekt, das zum Aufzählen der Zeilen der Ansicht verwendet werden kann.
5.  Verwenden Sie [](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) die ienumcertviewrow-Methoden [**ienumcertviewrow:: enumcertviewattribute**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewattribute), [**ienumcertviewrow:: enumcertviewcolumn**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewcolumn)und [**ienumcertviewrow:: enumcertviewextension**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewextension) zum Abrufen von Attribut-, Spalten-und Erweiterungs Daten nach Belieben.

 

 
