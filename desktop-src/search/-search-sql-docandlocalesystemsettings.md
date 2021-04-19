---
description: Wenn das Betriebssystem oder sogar eine Anwendung für die Verwendung einer bestimmten Sprache und eines bestimmten Gebiets Schemas festgelegt ist, sind viele Einstellungen betroffen.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Gebiets Schema Einstellungen für Dokumente und Systeme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9408093a8583a4b17566b5fcd118b30439c0ebda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350393"
---
# <a name="document-and-system-locale-settings"></a>Gebiets Schema Einstellungen für Dokumente und Systeme

Wenn das Betriebssystem oder sogar eine Anwendung für die Verwendung einer bestimmten Sprache und eines bestimmten Gebiets Schemas festgelegt ist, sind viele Einstellungen betroffen. Diese Einstellungen umfassen das numerische Format, das Datumsformat, das Währungs Format, die Zuordnung von Groß-und Kleinbuchstaben, die Sortierreihenfolge für Wörterbücher, die Tokenisierung und andere. Obwohl diese Einstellungen Windows Search helfen, eine hervorragende lokalisierte Unterstützung zu bieten, können unerwartete Ergebnisse auftreten, wenn Dokumente aus einem Gebiets Schema durchsucht werden, indem ein System verwendet wird, das auf ein anderes Gebiets Schema

Wenn das [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Objekt die Texteigenschaften und den Inhalt eines Dokuments verarbeitet, meldet es dem inhaltsindexer die Sprache des Dokuments. Mithilfe dieser Informationen kann Windows Search die entsprechende Wörter Trennung anwenden.

 

 
