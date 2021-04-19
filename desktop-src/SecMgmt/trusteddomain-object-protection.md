---
description: Wenn ein Treuhänder-Domänen Objekt erstellt wird, wird ihm ein Standardschutz zugewiesen.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: Schutz von treuhänddomain-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd27a01c1bcfde12fd062f2e8ae7c92a979991a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353038"
---
# <a name="trusteddomain-object-protection"></a>Schutz von treuhänddomain-Objekten

Wenn ein " [**Treuhänder**](trusteddomain-object.md) "-Objekt erstellt wird, wird ihm ein Standardschutz wie folgt zugewiesen:

-   Der lokalen Gruppe "World" wird generischer \_ Ausführungs Zugriff gewährt.
-   Der lokalen \_ Gruppe "Administratoren" werden löschen, generischer \_ Lesezugriff, generischer \_ Schreibzugriff und generischer \_ Ausführungs Zugriff gewährt.
-   Die lokale \_ Gruppe "Administratoren" wird als Besitzer und primäre Gruppe des Objekts zugewiesen.

 

 



