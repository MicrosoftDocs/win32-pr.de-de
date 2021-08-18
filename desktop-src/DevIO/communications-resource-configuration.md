---
description: Die COMMCONFIG-Struktur definiert die Konfiguration einer Kommunikationsressource, seriell oder anderweitig.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Konfiguration der Kommunikationsressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01cd85a60eabc3cf6adcbdb0e05d2fbdc662442029044a5ac67d9a37bc073d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918320"
---
# <a name="communications-resource-configuration"></a>Konfiguration der Kommunikationsressource

Die [**COMMCONFIG-Struktur**](/windows/desktop/api/Winbase/ns-winbase-commconfig) definiert die Konfiguration einer Kommunikationsressource, seriell oder anderweitig. Das Format der Struktur variiert je nach Typ der Kommunikationsressource (Anbieteruntertyp). Die ersten Strukturmitglieder sind allen Kommunikationsressourcen gemeinsam. zusätzliche Member werden für bestimmte Anbieteruntertypen definiert. Bestimmte Dienstanbieter können auch die **COMMCONFIG-Struktur** erweitern.

Eine Anwendung kann die Konfiguration einer Kommunikationsressource mithilfe der [**Funktionen GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) und [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) erhalten und festlegen. Beim Öffnen wird eine Kommunikationsressource mit der Standardkonfiguration für ihren Anbieteruntertyp initialisiert. Verwenden Sie zum Erhalten und Festlegen der Standardkonfiguration für einen Anbieteruntertyp die [**Funktionen GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) und [**SetDefaultCommConfig.**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)

Verwenden Sie die [**CommConfigDialog-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) um den Benutzer zur Eingabe von Konfigurationsinformationen aufforderungen. Diese Funktion zeigt ein vom Dienstanbieter definiertes Dialogfeld an und füllt eine [**COMMCONFIG-Struktur**](/windows/desktop/api/Winbase/ns-winbase-commconfig) basierend auf Benutzereingaben aus.

 

 



