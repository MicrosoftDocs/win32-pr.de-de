---
description: 'Mit den folgenden Funktionen kann eine Anwendung einen Gerätekontext speichern, wiederherstellen und zurücksetzen: savedc, restoredc und ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Speichern, wiederherstellen und Zurücksetzen eines Geräte Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979792"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a>Speichern, wiederherstellen und Zurücksetzen eines Geräte Kontexts

Mit den folgenden Funktionen kann eine Anwendung einen Gerätekontext speichern, wiederherstellen und zurücksetzen: [**savedc**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**restoredc**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)und [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca). Die savedc-Funktion zeichnet in einem speziellen GDI-Stapel die Grafik Objekte des aktuellen Domänen Controllers und deren Attribute und Grafikmodi auf. Eine Zeichnungsanwendung kann diese Funktion aufzurufen, bevor ein Benutzer mit der Zeichnung beginnt, den ursprünglichen Zustand der Anwendung zu speichern und einen sauberen Slate für den Benutzer bereitzustellen. Um in diesen ursprünglichen Zustand zurückzukehren, ruft die Anwendung die restoredc-Funktion auf.

[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) wird zum Zurücksetzen von Drucker-DC-Daten bereitgestellt. Eine Anwendung ruft diese Funktion auf, um die Papier Ausrichtung, die Papiergröße, den Ausgabe Skalierungsfaktor, die Anzahl der zu druckenden Kopien, die Papier Quelle (oder den bin), den Duplex Modus usw. zurückzusetzen. In der Regel Ruft eine Anwendung diese Funktion auf, nachdem ein Benutzer eine der Druckeroptionen geändert hat und das System eine [**WM \_ devmodechange**](wm-devmodechange.md) -Meldung ausgegeben hat.

 

 



