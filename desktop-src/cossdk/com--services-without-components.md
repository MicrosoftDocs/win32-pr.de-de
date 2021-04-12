---
description: Com+-Dienste ohne Komponenten
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Com+-Dienste ohne Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127041"
---
# <a name="com-services-without-components"></a>Com+-Dienste ohne Komponenten

Mit com+ 1,5 können Sie die von com+ bereitgestellten Dienste verwenden, ohne eine-Komponente zu erstellen, die die Methoden enthält, mit denen diese Dienste aufgerufen werden. Dadurch profitieren Sie von Entwicklern, die normalerweise keine Komponenten verwenden, aber com+-Dienste wie Transaktionen oder com+-Tracker verwenden möchten. Durch die Verwendung von COM+-Diensten ohne Komponenten können Entwickler den Aufwand vermeiden, mit dem eine Komponente erstellt wird, die nur für den Zugriff auf die benötigten com+-Dienste verwendet wird.

Beispielsweise waren Skript Umgebungen üblicherweise die größten Verbraucher von COM+-Diensten, Sie waren jedoch nie in der Lage, diese Dienste effizient zu nutzen, da die Dienste innerhalb einer COM+-Komponente gebündelt werden mussten. Diese Bündelung erfordert aufgrund der verstärkten Kommunikation und Duplizierung von Daten, die für die Interaktion der Skript Umgebung mit der Komponente erforderlich sind, zu Leistungseinbußen. Durch die Verwendung von Diensten ohne Komponenten werden solche Kosten minimiert.

Die in der folgenden Tabelle beschriebenen Themen enthalten Hintergrundinformationen und Aufgabeninformationen zur Verwendung von COM+-Diensten ohne Komponenten. Diese Funktion ist für erweiterte Visual C++ Entwickler gedacht, die sich Gedanken über die Leistung machen.



| Thema                                                                                                 | BESCHREIBUNG                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Konzepte der com+-Dienste ohne Komponenten](com--services-without-components-concepts.md)<br/> | Bietet einen Überblick über die Verwendung von COM+-Diensten ohne Komponenten.<br/>                     |
| [Com+-Dienste ohne Komponenten Aufgaben](com--services-without-components-tasks.md)<br/>       | Stellt Anweisungen für die Verwendung von com+ zum Erstellen und Verwenden von-Diensten ohne Komponenten bereit.<br/> |



 

 

 




