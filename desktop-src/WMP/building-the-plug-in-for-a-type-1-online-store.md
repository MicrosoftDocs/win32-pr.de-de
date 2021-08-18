---
title: Erstellen des Plug-Ins für einen Typ 1 Online Store
description: Erstellen des Plug-Ins für einen Typ 1 Online Store
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player Onlineshops, Plug-Ins
- Onlineshops, Plug-Ins
- Geben Sie 1 Onlineshops und Plug-Ins ein.
- Windows Media Player Onlineshops, Erstellen von Plug-Ins
- Onlineshops, Erstellen von Plug-Ins
- Geben Sie 1 Onlineshops ein, und erstellen Sie Plug-Ins.
- Windows Media Player Onlineshops, IWMPContentPartner-Schnittstelle
- Onlineshops, IWMPContentPartner-Schnittstelle
- Geben Sie 1 Onlineshops ein, IWMPContentPartner-Schnittstelle
- Plug-Ins, Windows Media Player Onlineshops
- Plug-Ins, Onlineshops
- Plug-Ins, Geben Sie 1 Onlineshop ein.
- Plug-Ins, IWMPContentPartner-Schnittstelle
- Plug-Ins, Erstellen
- Windows Media Player Plug-Ins, geben Sie 1 Onlineshop ein.
- Windows Media Player Plug-Ins, Onlineshops
- Windows Media Player Plug-Ins, Windows Media Player Onlineshops
- Windows Media Player-Plug-Ins, IWMPContentPartner-Schnittstelle
- Windows Media Player-Plug-Ins, Erstellen
- IWMPContentPartner
- Erstellen von Plug-Ins, Geben Sie 1 Onlineshops ein.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fdc5b01a0a8ec526af22e6be90c562524536cdb30b37bd03eb40132af0be49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997850"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a>Erstellen des Plug-Ins für einen Typ 1 Online Store

Ein Onlineshop vom Typ 1 muss ein Plug-In bereitstellen, das die [**IWMPContentPartner-Schnittstelle**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) implementiert. Das Plug-In wird in einem anderen Prozess als Windows Media Player ausgeführt.

Die Schritte zum Erstellen eines Plug-Ins, das außerhalb des Prozesses ausgeführt wird, sind wie folgt:

1.  Schreiben Sie Ihr Plug-In so, als wäre es ein PROZESS-COM-Server.
2.  Erstellen Sie einen **DllSurrogate-Registrierungseintrag** auf dem Computer des Benutzers. Der **Eintrag DllSurrogate** informiert die COM-Runtime darüber, dass Ihr Plug-In in einer Instanz des standardmäßigen DLL-Ersatzzeichens erstellt werden soll, dllhost.exe.

Ausführliche Informationen zum Registrieren Ihres Plug-Ins finden Sie unter [Registrierungsschlüssel und -einträge für einen Typ 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).

Sie müssen keinen Proxy- oder Stubcode für Ihr Plug-In erstellen. Die gesamte Marshallingunterstützung wird von Windows Media Player bereitgestellt.

Sie können den Assistenten für Onlineshop-Plug-Ins verwenden, um schnell ein Plug-In zu erstellen, das als Ausgangspunkt dient. Weitere Informationen finden Sie unter [Installieren des Online-Store-Plug-In-Assistenten.](installing-the-online-store-plug-in-wizard.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch für Onlineshops vom Typ 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




