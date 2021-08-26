---
title: Server-Side Configuration Benutzeroberfläche
description: Implementieren Sie eine Konfigurationsbenutzeroberfläche für den Server, indem Sie die COM-Schnittstelle IEAPProviderConfig implementieren.
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92bf6a1f5b5f0e1302e68dd8ca9070771bfbc7714759a384f67782ffdad6e2ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021810"
---
# <a name="server-side-configuration-user-interface"></a>Server-Side Configuration Benutzeroberfläche

Implementieren Sie eine Konfigurationsbenutzeroberfläche für den Server, indem Sie die COM-Schnittstelle [**IEAPProviderConfig implementieren.**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig) Diese COM-Schnittstelle wird von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) abgeleitet und fügt drei Methoden hinzu: [**IEAPProviderConfig::Initialize,**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) [**IEAPProviderConfig::ServerInvokeConfigUI**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)und [**IEAPProviderConfig::Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize).

Die Benutzeroberfläche sollte die Remoteverwaltung unterstützen. Anders ausgedrückt: Obwohl die Benutzeroberfläche das Authentifizierungsprotokoll auf dem Server konfiguriert, kann die Benutzeroberfläche selbst auf einem anderen Computer ausgeführt werden. Um die Remoteverwaltung zu unterstützen, trennen Sie den Benutzeroberflächencode von dem Code, der die Konfiguration tatsächlich ausführt. Der Konfigurationscode befindet sich auf dem Server, auf dem das Authentifizierungsprotokoll ausgeführt wird.

Verwenden Sie Active Template Library (ATL), um [**IEAPProviderConfig zu implementieren.**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig) Weitere Informationen finden Sie in der Beispielbenutzeroberfläche für die serverseitige Konfiguration im Sdk-Beispielverzeichnis. Der Klassenbezeichner (CLSID) für das Benutzeroberflächenobjekt der Konfiguration sollte in der Registrierung mit dem [Wertnamen RAS \_ EAP \_ VALUENAME \_ CONFIG \_ CLSID platziert werden.](authentication-protocol-registry-values.md) Weitere Informationen finden Sie unter [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).

Wenn der Benutzer im Dialogfeld Eigenschaften für Routing und RAS auf die Schaltfläche Konfigurieren für ein Authentifizierungsprotokoll klickt, überprüft das System, ob ein RAS \_ EAP \_ VALUENAME \_ CONFIG CLSID-Wert für dieses Authentifizierungsprotokoll in der Registrierung vorhanden \_ ist. Wenn ja, instanziiert COM das Benutzeroberflächenobjekt für die Konfiguration. Wenn das System die RAS EAP VALUENAME CONFIG CLSID in der Registrierung nicht finden kann und das System Zugriff auf \_ \_ \_ Verzeichnisdienste (DS) hat, versucht das System, das Objekt aus der \_ Klasse Store.

Wenn der Benutzer gleichzeitig mit mehreren Computern verbunden ist, werden mehrere Benutzeroberflächenobjekte für die Konfiguration instanziiert.

 

 