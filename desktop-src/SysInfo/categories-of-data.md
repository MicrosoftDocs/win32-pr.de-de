---
description: 'Bevor Daten in die Registrierung übertragen werden, sollte eine Anwendung die Daten in zwei Kategorien unterteilen: computerspezifische Daten und benutzerspezifische Daten.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Datenkategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4bf4abb7af2abf723aa42f3426c58230083d8e575dda176b8eeda0daecb36d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885851"
---
# <a name="categories-of-data"></a>Datenkategorien

Bevor Daten in die Registrierung übertragen werden, sollte eine Anwendung die Daten in zwei Kategorien unterteilen: computerspezifische Daten und benutzerspezifische Daten. Durch diese Unterscheidung kann eine Anwendung mehrere Benutzer unterstützen und dennoch benutzerspezifische Daten über ein Netzwerk suchen und diese Daten an verschiedenen Speicherorten verwenden, sodass standortunabhängige Benutzerprofildaten möglich sind. (Ein Benutzerprofil ist ein Satz von Konfigurationsdaten, die für jeden Benutzer gespeichert werden.)

Wenn die Anwendung installiert ist, sollte sie die computerspezifischen Daten unter dem **HKEY \_ LOCAL \_ MACHINE-Schlüssel** aufzeichnen. Insbesondere sollten Schlüssel für den Unternehmensnamen, den Produktnamen und die Versionsnummer erstellt werden, wie im folgenden Beispiel gezeigt:

**HKEY \_ LOCAL \_ MACHINE \\ \\ Software**_MyCompany \\ MyProduct \\ 1.0_

Wenn die Anwendung COM unterstützt, sollte sie diese Daten unter **HKEY \_ LOCAL MACHINE Software Classes \_ \\ \\ aufzeichnen.**

Eine Anwendung sollte benutzerspezifische Daten unter dem **HKEY \_ CURRENT \_ USER-Schlüssel** aufzeichnen, wie im folgenden Beispiel gezeigt:

**HKEY \_ CURRENT \_ USER \\ \\ Software**_MyCompany \\ MyProduct \\ 1.0_

 

 



