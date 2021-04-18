---
title: Entwickeln des Plug-Ins für einen Typ-1-Online Shop
description: Entwickeln des Plug-Ins für einen Typ-1-Online Shop
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player Online Stores, Plug-ins
- Online Stores, Plug-ins
- Typ 1 Online Stores, Plug-ins
- Windows Media Player Online Stores, Aufbau von Plug-ins
- Online Stores, Aufbau von Plug-ins
- Geben Sie 1 Online Stores ein, und entwickeln Sie Plug-ins.
- Windows Media Player Online Stores, iwmpcontentpartner-Schnittstelle
- Online Stores, iwmpcontentpartner-Schnittstelle
- Typ 1 Online Stores, iwmpcontentpartner-Schnittstelle
- Plug-ins, Windows Media Player Online Stores
- Plug-ins, Online Stores
- Plug-ins, Typ 1 Online Stores
- Plug-ins, iwmpcontentpartner-Schnittstelle
- Plug-ins, Gebäude
- Windows Media Player-Plug-ins, geben Sie 1 Online Stores ein.
- Windows Media Player-Plug-ins, Online Stores
- Windows Media Player-Plug-ins, Windows Media Player Online Stores
- Windows Media Player-Plug-ins, iwmpcontentpartner-Schnittstelle
- Windows Media Player-Plug-ins, Gebäude
- Iwmpcontentpartner
- Entwickeln von Plug-ins, eingeben von 1 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339044"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a>Entwickeln des Plug-Ins für einen Typ-1-Online Shop

Ein Onlinespeicher vom Typ 1 muss ein Plug-in bereitstellen, das die [**iwmpcontentpartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) -Schnittstelle implementiert. Das Plug-in wird in einem separaten Prozess von Windows Media Player ausgeführt.

Die Schritte zum Erstellen eines Plug-ins, das außerhalb des Prozesses ausgeführt wird, lauten wie folgt:

1.  Schreiben Sie Ihr Plug-in so, als wäre es ein Prozess interner com-Server.
2.  Erstellen Sie einen **dllersatz** -Registrierungs Eintrag auf dem Computer des Benutzers. Der **dllersatz** -Eintrag informiert die com-Laufzeit darüber, dass das Plug-in in einer Instanz des standardmäßigen dll-Ersatz Zeichens (dllhost.exe) erstellt werden soll.

Ausführliche Informationen zum Registrieren des Plug-Ins finden Sie unter [Registrierungsschlüssel und Einträge für den Online Store vom Typ 1](registry-keys-and-entries-for-a-type-1-online-store.md).

Sie müssen keinen Proxy-oder Stubcode für Ihr Plug-in erstellen. Alle Marshallingunterstützung wird von Windows Media Player bereitgestellt.

Mit dem Assistenten für Online Shop-Plug-Ins können Sie schnell ein Plug-in erstellen, das als Ausgangspunkt fungiert. Weitere Informationen finden Sie unter [Installieren des Plug-in-Assistenten für den Online Shop](installing-the-online-store-plug-in-wizard.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für den Typ 1 Online Stores**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




