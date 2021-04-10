---
description: Die CommConfig-Struktur definiert die Konfiguration einer Kommunikations Ressource, seriell oder anderweitig.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Kommunikationsressourcen Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126800"
---
# <a name="communications-resource-configuration"></a>Kommunikationsressourcen Konfiguration

Die [**CommConfig**](/windows/desktop/api/Winbase/ns-winbase-commconfig) -Struktur definiert die Konfiguration einer Kommunikations Ressource, seriell oder anderweitig. Das Format der Struktur variiert abhängig vom Typ der Kommunikations Ressource (Anbieter Untertyp). Die ersten Strukturmember sind von allen Kommunikationsressourcen gemeinsam. für bestimmte Anbieter Untertypen werden zusätzliche Member definiert. Bestimmte Dienstanbieter können auch die **CommConfig** -Struktur erweitern.

Eine Anwendung kann die Konfiguration einer Kommunikations Ressource mithilfe der Funktionen [**getcommconfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) und [**setcommconfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) erhalten und festlegen. Beim Öffnen wird eine Kommunikations Ressource mit der Standardkonfiguration für den Anbieter Untertyp initialisiert. Um die Standardkonfiguration für einen Anbieter Untertyp abzurufen und festzulegen, verwenden Sie die Funktionen [**getdefaultcommconfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) und [**setdefaultcommconfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .

Um den Benutzer zur Eingabe von Konfigurationsinformationen aufzufordern, verwenden Sie die [**commconfigdialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) -Funktion. Diese Funktion zeigt ein vom Dienstanbieter definiertes Dialogfeld an und füllt eine [**CommConfig**](/windows/desktop/api/Winbase/ns-winbase-commconfig) -Struktur auf Grundlage von Benutzereingaben aus.

 

 



