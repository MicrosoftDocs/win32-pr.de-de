---
description: Während einer Windows Installer Installation kann das Installationsprogramm nach einem Registrierungs Eintrag suchen und eine Eigenschaft erstellen, die den Wert der Registrierung enthält.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Suchen nach einem Registrierungs Eintrag und Erstellen einer Eigenschaft mit dem Wert der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862039"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a>Suchen nach einem Registrierungs Eintrag und Erstellen einer Eigenschaft mit dem Wert der Registrierung

**So suchen Sie nach einem Registrierungs Eintrag und erstellen eine Eigenschaft, die den Wert dieser Datei enthält**

1.  Fügen Sie die Signatur der [Signatur Tabelle](signature-table.md) oder der Tabelle " [complocator](complocator-table.md)" nicht hinzu. Wenn eine Datei Signatur in der Tabelle " [AppSearch](appsearch-table.md) " aufgeführt ist und nicht in den Tabellen "Signature" oder "complocator" aufgeführt ist, sucht das Installationsprogramm in der [Tabelle "reglocator](reglocator-table.md)".

2.  Geben Sie den Registrierungs Eintrag an, nach dem in der [reglocator-Tabelle](reglocator-table.md)gesucht werden soll. Wenn die Signatur in der [Signatur Tabelle](signature-table.md) nicht vorhanden ist und der Wert der Type-Spalte **msidblocatortyperawvalue** ist, wird angenommen, dass die Suche für den spezifischen Registrierungsschlüssel Namen erfolgt, auf den die reglocator-Tabelle verweist.

    [Reglocator-Tabelle](reglocator-table.md) (partiell)

    

    | Signatur\_         | Root         | Schlüssel                                                           | Name                  | type                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | Appvalue<br/> | 2<br/> | **Software** \\ **Microsoft** \\ **Myapp**<br/> <br/> | **"Myname"**<br/> | **msidbloserortyperawvalue**<br/> |

    

     

3.  Füllen Sie schließlich die [AppSearch-Tabelle](appsearch-table.md) auf, damit die [AppSearch-Aktion](appsearch-action.md) den Wert von appvalue zurückgibt. Nachdem das Installationsprogramm die AppSearch-Aktion ausgeführt hat, ist der Wert von myregval der Wert von appvalue.

    [AppSearch-Tabelle](appsearch-table.md) (partiell)

    

    | Eigenschaft            | Signatur           |
    |---------------------|---------------------|
    | Myregval<br/> | Appvalue<br/> |

    

     

 

 




