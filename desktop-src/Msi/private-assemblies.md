---
description: Eine Win32-Assembly kann als private Assembly installiert werden und ist ausschließlich für die Verwendung durch eine Anwendung verfügbar. Private Assemblys sollten von einem Windows Installer-Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Private Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cc9bd9c9f4c5230dcb24ed7059f6817d4c5f3c7cfdeb4b7cfd25d95ca2a3eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327844"
---
# <a name="private-assemblies"></a>Private Assemblys

Eine Win32-Assembly kann als private Assembly installiert werden und ist ausschließlich für die Verwendung durch eine Anwendung verfügbar. Private Assemblys sollten von einem Windows Installer-Paket installiert werden, das zum Installieren oder Aktualisieren einer Anwendung verwendet wird.

Auf Windows XP werden private Assemblys als [nebenseitige Assemblys](side-by-side-assemblies.md)installiert. Der Windows Installer installiert private parallele Assemblys in einem Ordner, der für die Anwendung privat ist. In der Regel der Ordner, der die ausführbare Datei der Anwendung enthält. Die Abhängigkeit der Anwendung von der privaten Assembly wird in einer Anwendungsmanifestdatei angegeben. Weitere Informationen finden Sie unter [Isolierte Anwendungen und Nebenassemblys.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

Unter Betriebssystemen vor Windows XP wird eine Kopie der privaten Assembly und einer LOKALEN Datei zur exklusiven Verwendung der Anwendung in einem privaten Ordner installiert. Eine Version der Assembly ist auch global auf dem System registriert und für jede Anwendung verfügbar, die an sie gebunden ist. Die globale Version der Assembly kann die Version sein, die mit der Anwendung oder einer früheren Version installiert wurde. Die globale Version wird durch die gleichen Regeln bestimmt, die von [isolierten Komponenten](isolated-components.md)verwendet werden.

Beachten Sie, dass der Windows Installer keine private Assembly an einem Speicherort mit einem Pfad installieren kann, der mehr als 234 Zeichen enthält, einschließlich des abschließenden NULL-Zeichens.

 

 
