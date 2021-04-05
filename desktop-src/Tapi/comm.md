---
description: Die comm-Geräteklasse besteht aus Kommunikationsports. Sie greifen auf diese Geräte mithilfe der Datei-und Kommunikationsfunktionen zu.
ms.assetid: c1cf4998-b752-4cfd-9dd7-c9872b62c44b
title: Komm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40136654d7e308f30e4e27467cf5e21385340841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753000"
---
# <a name="comm"></a>Komm

Die comm-Geräteklasse besteht aus Kommunikationsports. Sie greifen auf diese Geräte mithilfe der [Datei](/windows/desktop/FileIO/file-management-functions) -und [Kommunikationsfunktionen](/windows/desktop/DevIO/communications-functions)zu.

Die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt den **dwstringformat** -Member auf den \_ ASCII-Wert StringFormat fest und fügt eine NULL-terminierte Zeichenfolge an, die den Namen des kommunikationsgeräts angibt (z. b. den Modem Namen).

 

 
