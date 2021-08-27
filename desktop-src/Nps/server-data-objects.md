---
title: Serverdatenobjekte
description: Mit der SDO-API (Server Data Objects) können Sie ein System, auf dem NPS ausgeführt wird, programmgesteuert konfigurieren und verwalten.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d51c4a8b04b9da6994daa4941d255f0d74f68ea858d4a3909ed9ecc1ae28514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128410"
---
# <a name="server-data-objects"></a>Serverdatenobjekte

> [!Note]  
> Internet Authentication Service (IAS) wurde ab Windows Server 2008 in Network Policy Server (NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Mit der SDO-API (Server Data Objects) können Sie ein System, auf dem NPS ausgeführt wird, programmgesteuert konfigurieren und verwalten. Mithilfe von SDO kann ein Entwickler auch Anwendungen schreiben, die Richtlinien und Profile für den Remotezugriff verwalten. Die Remotezugriffsrichtlinien und -profile werden vom Routing- und Ras-Dienst (RRAS) sowie nps verwendet, um zu bestimmen, ob ein Remoteclient eine Verbindung mit einem Netzwerkzugriffsserver (NAS) herstellen darf.

Die SDO-API ist in jeder Umgebung anwendbar, die NPS oder RAS-Richtlinien verwendet.

Mit der SDO-API kann ein Entwickler jedes Element der NPS-Konfiguration bearbeiten, auf das über die NPS-Benutzeroberfläche zugegriffen werden kann.

Die SDO-API ermöglicht auch das Festlegen oder Abrufen aller Werte, auf die über die Eigenschaftenseite der Benutzer-Einwahleinstellungen zugegriffen werden kann.

Die SDO-API besteht aus COM-Schnittstellen. Jede der Schnittstellen in der SDO-API erbt von der COM [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Mit **der IDispatch-Schnittstelle** können Entwickler die SDO-Schnittstellenmethoden von Visual Basic oder einem beliebigen Automation-Client sowie von C/C++ aufrufen.

Entwickler können die SDO-API auch über Skriptsprachen wie VBScript aufrufen. Da VBScript jedoch nur auf die Verwendung von VARIANT-Parametern beschränkt ist, sind nicht alle Funktionen von SDO verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

[Übersicht](/windows/desktop/Nps/sdo-about-server-data-objects)

Allgemeine Informationen zur Server Data Objects-API.

[Mit](/windows/desktop/Nps/sdo-using-server-data-objects)

Beispielcode, der die Verwendung der Serverdatenobjekt-API veranschaulicht.

[Referenz](/windows/desktop/Nps/sdo-server-data-objects-reference)

Dokumentation der aufzählten Typen und Schnittstellen, aus denen die Serverdatenobjekt-API erstellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerkrichtlinienserver (Internetauthentifizierungsdienst)](portal.md)
</dt> <dt>

[Remotezugriffsdienst](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 