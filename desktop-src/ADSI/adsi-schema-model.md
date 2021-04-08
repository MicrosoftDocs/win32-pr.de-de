---
title: ADSI-Schema Modell
description: Ein Schema ähnelt einem Wörterbuch darin, dass es die Definition aller Typen von Objekten enthält, die einem Verzeichnisdienst bekannt sind.
ms.assetid: 70561a11-1560-4b1c-a999-e2a7b2002ab0
ms.tgt_platform: multiple
keywords:
- ADSI-Schema Modell ADSI
- ADSI ADSI, Info, Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23eec9264ae2692952106802cc06cbad937a42a9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949109"
---
# <a name="adsi-schema-model"></a>ADSI-Schema Modell

Ein Schema ähnelt einem Wörterbuch darin, dass es die Definition aller Typen von Objekten enthält, die einem Verzeichnisdienst bekannt sind. ADSI-Client Anwendungen können ein Schema durchsuchen, um die Funktionen einer beliebigen ADSI-Implementierung zu ermitteln. Außerdem bietet ADSI Schema Verwaltungs Schnittstellen, die für die Kommunikation mit dem zugrunde liegenden Schema eines Verzeichnis Dienstanbieters verwendet werden können.

Einige Schemas sind erweiterbare und ADSI-Anbieter oder Drittanbieter können neue Schnittstellen oder zusätzliche Eigenschaften für vorhandene Schnittstellen dort veröffentlichen. ADSI-Clients verwenden diese Daten, um zu bestimmen, welche Funktionen für die einzelnen Verzeichnisdienste unterstützt werden.

Es gibt drei Arten von Schema Objekten: Klassen, Eigenschaften und Syntaxen, die jeweils die Schema Verwaltungs Schnittstellen [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)und [**iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)unterstützen.

> [!Note]  
> Die Klasse ist ein überladener Begriff. Es gibt C++-Klassen, Java-Klassen, com-Klassen und ADSI-Klassen. In diesem Dokument bezieht sich die Word-Klasse, sofern nicht anders qualifiziert, auf eine Kategorie oder einen Typ von Schema Objekten.

 

ADSI abstrahiert das Schema aller Verzeichnisdienste und platziert es in jedem Stamm Knoten der obersten Ebene im **Namespace** -Objekt. Um zu ermitteln, welche Klassen ein Verzeichnisdienst für einen bestimmten Stamm Knoten unterstützt, können Sie das Schema Objekt auflisten und eine Liste von Klassen Objekten, Eigenschafts Objekten und Syntax Objekten erhalten. Weitere Informationen finden Sie unter [Verwenden des ADSI-Schemas](using-the-adsi-schema.md).

## <a name="adsi-ldap-provider-schema-cache"></a>Schema Cache des ADSI LDAP-Anbieters

Der LDAP-Anbieter für ADSI versucht, Schema Daten auf dem lokalen Computer zwischenzuspeichern. Ein unter Schema wird durch einen Distinguished Name identifiziert, der im [**subschemasubentry**](/windows/desktop/ADSchema/a-subschemasubentry) -Attribut gespeichert ist, das sich im Stammverzeichnis des Verzeichnisdienst Enterprise (RootDSE) befindet. Zusätzlich zur Bereitstellung der unter Schema Daten sollten LDAP-V3-Server ein [**modifytimestamp**](/windows/desktop/ADSchema/a-modifytimestamp) -Attribut verfügbar machen, mit dem bestimmt wird, wann das Schema zuletzt geändert wurde.

Wenn ADSI zuerst eine Bindung an den LDAP-Server herstellt, ruft es die unter Schema Daten mithilfe des [**subschemasubentry**](/windows/desktop/ADSchema/a-subschemasubentry) -Attributs ab. Wenn ADSI das unter Schema Objekt nicht finden kann, speichert es einen Zeiger auf die Daten in der Registrierung auf dem Computer, der eine Verbindung mit dem LDAP-Server herstellt. Informationen dazu, wo diese Werte genau in der Registrierung gespeichert sind, finden Sie unter [ADSI und Benutzerkontensteuerung](adsi-and-uac.md).

ADSI versucht dann, die Schema Daten zu verarbeiten und liest das [**modifytimestamp**](/windows/desktop/ADSchema/a-modifytimestamp) -Attribut. Wenn das **modifytimestamp** -Attribut vorhanden ist und ADSI das Schema erfolgreich verarbeitet hat, schreibt ADSI das unter Schema auf den Datenträger und erstellt die beiden folgenden Registrierungs Werte unter dem Schlüssel. Wenn die unter Schema Daten vorhanden sind, aber nicht verarbeitet werden können, werden keine dieser Registrierungs Werte erstellt:

-   Ein **Uhrzeitwert** , der das [**modifytimestamp**](/windows/desktop/ADSchema/a-modifytimestamp) -Attribut enthält. Dieser Wert wird verwendet, um sicherzustellen, dass die Schema Daten aktuell sind, und verhindert das Konstante erneute Laden der Schema Daten.
-   Ein **Dateiwert** , der den Pfad enthält, unter dem ADSI die Schema Daten im Dateisystem speichert. Standardmäßig speichert ADSI das unter Schema im Verzeichnis " <systemroot> \\ schcache" mit einem Dateinamen, der dem Namen des LDAP-Servers entspricht.

Wenn die unter Schema Daten verarbeitet werden können, aber kein [**modifytimestamp**](/windows/desktop/ADSchema/a-modifytimestamp) -Attribut verfügbar gemacht wird, werden die Schema Daten im Arbeitsspeicher zwischengespeichert, aber nicht auf den Datenträger geschrieben. Wenn ein LDAP-V3-Server über ADSI auf dem lokalen Computer kontaktiert wurde und kein zwischengespeichertes unter Schema vorhanden ist, hat dies wahrscheinlich einen der folgenden Gründe:

-   Der Server hat die richtigen Eigenschaften nicht verfügbar gemacht.
-   ADSI konnte das Schema nicht verarbeiten.
-   ADSI konnte die Datei nicht in das Dateisystem schreiben.

 

 