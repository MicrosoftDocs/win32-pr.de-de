---
title: Server-Side Konfigurations Benutzeroberfläche
description: Implementieren Sie eine Konfigurations Benutzeroberfläche für den Server, indem Sie die COM-Schnittstelle ieapproviderconfig implementieren.
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0904c90fea2bef3ccc00c00135be09a711d8454
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314967"
---
# <a name="server-side-configuration-user-interface"></a>Server-Side Konfigurations Benutzeroberfläche

Implementieren Sie eine Konfigurations Benutzeroberfläche für den Server, indem Sie die COM-Schnittstelle [**ieapproviderconfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig)implementieren. Diese COM-Schnittstelle wird von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) abgeleitet und fügt drei Methoden hinzu: [**ieapproviderconfig:: Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize), [**ieapproviderconfig:: serverinvokeconfigui**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)und [**ieapproviderconfig:: Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize).

Die Benutzeroberfläche sollte die Remote Verwaltung unterstützen. Mit anderen Worten: Obwohl die Benutzeroberfläche das Authentifizierungsprotokoll auf dem Server konfiguriert, wird die Benutzeroberfläche möglicherweise auf einem anderen Computer ausgeführt. Um die Remote Verwaltung zu unterstützen, trennen Sie den UI-Code von dem Code, der die Konfiguration tatsächlich ausführt. Der Konfigurations Code befindet sich auf dem Server, auf dem das Authentifizierungsprotokoll ausgeführt wird.

Verwenden Sie die Active Template Library (ATL), um [**ieapproviderconfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig)zu implementieren. Weitere Informationen finden Sie in der Beispiel-Benutzeroberfläche für die serverseitige Konfiguration im SDK samples-Verzeichnis. Der Klassen Bezeichner (CLSID) für das Konfigurations-UI-Objekt sollte in der Registrierung mit dem Namen " [RAS \_ EAP \_ valueName \_ config \_ CLSID](authentication-protocol-registry-values.md)" platziert werden. Weitere Informationen finden Sie unter [Registrierungs Werte für das Authentifizierungsprotokoll](authentication-protocol-registry-values.md).

Wenn der Benutzer im Dialogfeld Eigenschaften für Routing und RAS auf die Schaltfläche Konfigurieren für ein Authentifizierungsprotokoll klickt, prüft das System, ob \_ für dieses Authentifizierungsprotokoll ein RAS-EAP \_ valueName- \_ Konfigurations- \_ CLSID-Wert in der Registrierung vorhanden ist. Wenn dies der Fall ist, instanziiert com das Konfigurations-UI-Objekt. Wenn das System RAS \_ -EAP \_ valueName \_ config \_ CLSID in der Registrierung nicht finden kann und das System Zugriff auf Verzeichnisdienste (DS) hat, versucht das System, das Objekt aus dem Klassen Speicher zu instanziieren.

Wenn der Benutzer gleichzeitig mit mehreren Computern verbunden ist, werden mehrere Konfigurations-UI-Objekte instanziiert.

 

 