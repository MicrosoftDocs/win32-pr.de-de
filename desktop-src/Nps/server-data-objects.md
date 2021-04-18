---
title: Server Datenobjekte
description: Die Server Data Objects (SDO)-API ermöglicht die programmgesteuerte Konfiguration und Verwaltung eines Systems, auf dem NPS ausgeführt wird.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337446"
---
# <a name="server-data-objects"></a>Server Datenobjekte

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Die Server Data Objects (SDO)-API ermöglicht die programmgesteuerte Konfiguration und Verwaltung eines Systems, auf dem NPS ausgeführt wird. Mithilfe von SDO kann ein Entwickler auch Anwendungen schreiben, die RAS-Richtlinien und-Profile verwalten. Die RAS-Richtlinien und-Profile werden vom Routing-und RAS-Dienst (RRAS) sowie von NPS verwendet, um zu bestimmen, ob ein Remote Client eine Verbindung mit einem Netzwerk Zugriffs Server (NAS) herstellen darf.

Die SDO-API ist in jeder Umgebung anwendbar, die NPS oder RAS-Richtlinien verwendet.

Mithilfe der SDO-API kann ein Entwickler jedes beliebige Element der NPS-Konfiguration bearbeiten, auf das über die NPS-Benutzeroberfläche zugegriffen werden kann.

Mithilfe der SDO-API können auch alle Werte festgelegt oder abgerufen werden, auf die über die Eigenschaften Seite Benutzer-Einwähleinstellungen zugegriffen werden kann.

Die SDO-API besteht aus COM-Schnittstellen. Jede der Schnittstellen in der SDO-API erbt von der com- [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. Die **IDispatch** -Schnittstelle ermöglicht es Entwicklern, die Methoden der SDO-Schnittstelle von Visual Basic oder einem beliebigen Automatisierungs Client sowie von C/C++ aufzurufen.

Entwickler können die SDO-API auch aus Skriptsprachen wie VBScript abrufen. Da VBScript jedoch nur die Verwendung von Variant-Typparametern beschränkt, sind nicht alle Funktionen von SDO verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

[Übersicht](/windows/desktop/Nps/sdo-about-server-data-objects)

Allgemeine Informationen zur Server Data Objects-API.

[Genutzt](/windows/desktop/Nps/sdo-using-server-data-objects)

Beispielcode, der die Verwendung der Server Data Objects-API veranschaulicht.

[Verweis](/windows/desktop/Nps/sdo-server-data-objects-reference)

Dokumentation der enumerierten Typen und Schnittstellen, die die Server Data Objects-API bilden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk Richtlinien Server (Internet Authentication Service)](portal.md)
</dt> <dt>

[RAS-Dienst](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 