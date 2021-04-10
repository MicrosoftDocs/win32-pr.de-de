---
description: Der Windows Installer organisiert eine Installation der Konzepte von Komponenten und Features.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Komponenten und Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130293"
---
# <a name="components-and-features"></a>Komponenten und Features

Der Windows Installer organisiert eine Installation der Konzepte von Komponenten und Features.

Ein Feature ist ein Teil der Gesamtfunktionalität der Anwendung, die ein Benutzer unabhängig voneinander installieren kann. Weitere Informationen finden Sie unter [Windows Installer Features](windows-installer-features.md).

Eine Komponente ist ein Teil der zu installierenden Anwendung oder des Produkts. Das Installationsprogramm installiert oder entfernt eine Komponente immer als ein zusammenhängendes Element vom Computer eines Benutzers. Komponenten werden in der Regel für den Benutzer ausgeblendet. Wenn ein Benutzer eine Funktion für die Installation auswählt, legt das Installationsprogramm fest, welche Komponenten installiert werden müssen, um dieses Feature bereitzustellen. Weitere Informationen finden Sie unter [Windows Installer-Komponenten](windows-installer-components.md).

Autoren von Installationspaketen müssen entscheiden, wie die Anwendung in Funktionen und Komponenten aufgeteilt werden soll. Die Auswahl der Features hängt hauptsächlich von der Funktionalität der Anwendung aus der Perspektive des Benutzers ab. Da Komponenten in der Regel über mehrere Anwendungen oder sogar über Produkte hinweg gemeinsam genutzt werden müssen, empfiehlt es sich, dass die Autoren eine Standardmethode für die Auswahl von Komponenten befolgen. Weitere Informationen finden Sie unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md).

 

 



