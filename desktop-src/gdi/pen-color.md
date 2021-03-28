---
description: Das Color-Attribut gibt die Stift Farbe an.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Stift Farbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d831994ac444207832574dc104a9d5c2582db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528301"
---
# <a name="pen-color"></a>Stift Farbe

Das Color-Attribut gibt die Stift Farbe an. Eine Anwendung kann einen kosmetischen Stift mit einer eindeutigen Farbe erstellen, indem das [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) -Makro verwendet wird, um das rote, grüne und blaue Dreieck zu speichern, das die gewünschte Farbe in einer [COLORREF](colorref.md) -Struktur angibt und die Adresse dieser Struktur an die Funktion [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**createpenindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)oder [**extcreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) übergibt. (Die Stock Stifte sind auf schwarz, weiß und unsichtbar beschränkt.) Weitere Informationen zu RGB-drei-und-Farben finden Sie unter [Farben](colors.md).

 

 



