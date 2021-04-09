---
title: Konzepte der C++-und OLE-Programmierung
description: Konzepte der C++-und OLE-Programmierung
ms.assetid: 2c6c3f29-aa5d-4e55-8c4d-16c5fb223fb9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c47ef5ff2d89930b5d4138f12e3ebc15385a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856944"
---
# <a name="c-and-ole-programming-concepts"></a>Konzepte der C++-und OLE-Programmierung

Die in Windows enthaltenen Datei-und Datenstrom Handler verwenden einen objektorientierten Entwurf zum herauf Stufen einer Standardschnittstelle und zum Freigeben von Funktionen. Diese Handler sind in C++ geschrieben und verwenden die OLE-Component Object Model.

Sie können benutzerdefinierte Handler mithilfe der C-oder C++-Entwicklungssysteme entwickeln; Allerdings wird die Verwendung von C++ dringend empfohlen, da Sie einen einfacheren und einfacheren Ansatz zum Implementieren eines Handlers bereitstellt. Mit C++ können Sie Daten explizit als Objekte definieren, und Sie können die Funktionen, die die Daten bearbeiten, mit den Element Funktionen eines Objekts verknüpfen.

Dieser Abschnitt enthält eine kurze Zusammenfassung der wichtigen Konzepte von C++ und der OLE-Component Object Model, die für das Entwerfen und Implementieren von Datei-und streamhandlern gelten. Es gibt zahlreiche Bücher über C++ Programming, auf die Sie verweisen können, um weitere Informationen zu erhalten. Weitere Informationen zu OLE finden Sie in der *OLE-Programmier Referenz*.

 

 




