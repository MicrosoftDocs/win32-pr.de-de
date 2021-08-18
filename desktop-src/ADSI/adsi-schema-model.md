---
title: ADSI-Schemamodell
description: Ein Schema ähnelt einem Wörterbuch, da es die Definition jedes Objekttyps enthält, der einem Verzeichnisdienst bekannt ist.
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI-Schemamodell ADSI
- ADSI ADSI , about, schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfd8c06d10e05c11b2cc7c578814bb4ded2d897d3b7913b9b3d341a8a6c49086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023748"
---
# <a name="adsi-schema-model"></a>ADSI-Schemamodell

Ein Schema ähnelt einem Wörterbuch, da es die Definition jedes Objekttyps enthält, der einem Verzeichnisdienst bekannt ist. ADSI-Clientanwendungen können ein Schema durchsuchen, um die Features einer bestimmten ADSI-Implementierung zu entdecken. Darüber hinaus stellt ADSI Schemaverwaltungsschnittstellen bereit, die für die Kommunikation mit dem zugrunde liegenden Schema eines Verzeichnisdiensts verwendet werden können.

Einige Schemas sind erweiterbar, und ADSI-Anbieter oder Drittanbieter können sich dafür entscheiden, neue Schnittstellen oder zusätzliche Eigenschaften für vorhandene Schnittstellen dort zu veröffentlichen. ADSI-Clients verwenden diese Daten, um zu bestimmen, welche Features für jeden Verzeichnisdienst unterstützt werden.

Es gibt drei Arten von Schemaobjekten: Klassen, Eigenschaften und Syntaxen, die jeweils die Schemaverwaltungsschnittstellen [**IADsClass,**](/windows/desktop/api/Iads/nn-iads-iadsclass) [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)und [**IADsSyntax unterstützen.**](/windows/desktop/api/Iads/nn-iads-iadssyntax)

> [!Note]  
> Klasse ist ein überladener Begriff. Es gibt C++-Klassen, Java-Klassen, COM-Klassen und ADSI-Klassen. In diesem Dokument bezieht sich die Wortklasse, sofern nicht anders qualifiziert, auf eine Kategorie oder einen Typ des Schemaobjekts.

 

ADSI abstrahiert das Schema jedes Verzeichnisdiensts und platziert es in jedem Stammknoten der obersten Ebene im **Namespace-Objekt.** Um zu ermitteln, welche Klassen ein Verzeichnisdienst auf einem bestimmten Stammknoten unterstützt, listen Sie das Schemaobjekt auf und erhalten eine Liste von Klassenobjekten, Eigenschaftenobjekten und Syntaxobjekten. Weitere Informationen finden Sie unter [Verwenden des ADSI-Schemas.](using-the-adsi-schema.md)

## <a name="adsi-ldap-provider-schema-cache"></a>ADSI LDAP Provider Schema Cache

Der LDAP-Anbieter für ADSI versucht, Schemadaten auf dem lokalen Computer zwischenspeichern. Ein Unterschema wird durch einen Distinguished Name identifiziert, der im [**subSchemaSubEntry-Attribut**](/windows/desktop/ADSchema/a-subschemasubentry) im Stammverzeichnis des Verzeichnisdienstunternehmens (rootDSE) gespeichert ist. Zusätzlich zur Bereitstellung der Unterschemadaten sollten LDAP v3-Server ein [**modifyTimeStamp-Attribut**](/windows/desktop/ADSchema/a-modifytimestamp) verfügbar machen, mit dem bestimmt wird, zu welchem Zeitpunkt das Schema zuletzt geändert wurde.

Wenn ADSI zum ersten Mal an den LDAP-Server gebunden wird, ruft es die Unterschemadaten mithilfe des [**subSchemaSubEntry-Attributs**](/windows/desktop/ADSchema/a-subschemasubentry) ab. Wenn ADSI das Unterschemaobjekt erfolgreich findet, wird ein Zeiger auf die Daten in der Registrierung auf dem Computer gespeichert, der eine Verbindung mit dem LDAP-Server herstellen soll. Informationen dazu, wo genau diese Werte in der Registrierung gespeichert sind, finden Sie unter [ADSI und Benutzerkontensteuerung](adsi-and-uac.md).

ADSI versucht dann, die Schemadaten zu verarbeiten, und liest das [**modifyTimeStamp-Attribut.**](/windows/desktop/ADSchema/a-modifytimestamp) Wenn das **modifyTimeStamp-Attribut** vorhanden ist und ADSI das Schema erfolgreich verarbeitet, schreibt ADSI das Unterschema auf den Datenträger und erstellt die beiden folgenden Registrierungswerte unter dem Schlüssel. Wenn die Unterschemadaten vorhanden sind, aber nicht verarbeitet werden können, wird keiner dieser Registrierungswerte erstellt:

-   Ein **Time-Wert,** der das [**modifyTimeStamp-Attribut**](/windows/desktop/ADSchema/a-modifytimestamp) enthält. Dieser Wert wird verwendet, um sicherzustellen, dass die Schemadaten aktuell sind, und verhindert das konstante erneute Laden der Schemadaten.
-   Ein **Dateiwert,** der den Pfad enthält, unter dem ADSI die Schemadaten im Dateisystem speichert. Standardmäßig speichert ADSI das Unterschema im SchCache-Verzeichnis mit einem Dateinamen zwischen, der dem Namen des <systemroot> \\ LDAP-Servers entspricht.

Wenn die Unterschemadaten verarbeitet werden können, aber kein [**modifyTimeStamp-Attribut**](/windows/desktop/ADSchema/a-modifytimestamp) verfügbar gemacht wird, werden die Schemadaten im Arbeitsspeicher zwischengespeichert, aber nicht auf den Datenträger geschrieben. Wenn ein LDAP v3-Server über ADSI auf dem lokalen Computer kontaktiert wurde und kein zwischengespeichertes Unterschema vorhanden ist, hat dies wahrscheinlich einen der folgenden Gründe:

-   Der Server hat nicht die richtigen Eigenschaften verfügbar gemacht.
-   ADSI konnte das Schema nicht verarbeiten.
-   ADSI konnte die Datei nicht in das Dateisystem schreiben.

 

 