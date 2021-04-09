---
description: Auflisten von Geräten und Filtern
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Auflisten von Geräten und Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860408"
---
# <a name="enumerating-devices-and-filters"></a>Auflisten von Geräten und Filtern

Manchmal muss eine Anwendung einen bestimmten Filter im System des Benutzers suchen. Beispielsweise wird in einer Video Erfassungs Anwendung möglicherweise eine Liste der verfügbaren Erfassungsgeräte angezeigt. Da DirectShow eine komponentenbasierte Architektur verwendet, können Sie zur Entwurfszeit nicht wissen, welche Filter auf dem System des Benutzers installiert werden. Dies gilt insbesondere für Filter, die Hardware Geräte darstellen. DirectShow bietet zwei Komponenten, die registrierte Filter finden:

-   Der [Enumerator für System Geräte](system-device-enumerator.md) findet Filter nach ihrer Kategorie.
-   Der [Filter Mapper](filter-mapper.md) findet Filter gemäß den Suchkriterien, die von der Anwendung bereitgestellt werden.

Die in diesem Abschnitt erläuterten Enumeratoren befolgen das Standardformular, das von com-enumerationsschnittstellen verwendet wird. Weitere Informationen finden Sie im Thema "IEnumXXXX" im Microsoft Platform Software Development Kit (SDK).

Dieser Abschnitt enthält die folgenden Themen:

-   [Verwenden des Enumerators für System Geräte](using-the-system-device-enumerator.md)
-   [Verwenden des Filter Mappers](using-the-filter-mapper.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> </dl>

 

 



