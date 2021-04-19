---
description: Im Gegensatz zum Löschen einer dynamischen Instanz ist das Löschen einer Klasse eine einfache Prozedur.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Löschen einer Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355293"
---
# <a name="deleting-a-class"></a>Löschen einer Klasse

Im Gegensatz zum Löschen einer dynamischen Instanz ist das Löschen einer Klasse eine einfache Prozedur. Wie bereits erläutert, werden Basisklassen oder abgeleitete Klassen jedoch nur selten gelöscht. Stattdessen wird eine Instanz häufiger gelöscht. Die [Skript-API für WMI](scripting-api-for-wmi.md) verwendet dieselben Methoden, um entweder ein Klassenobjekt oder eine Instanz zu löschen. Weitere Informationen finden Sie unter [Löschen einer Instanz](deleting-an-instance.md). Weitere Informationen zum Entfernen von Klassen und Instanzen aus dem WMI-Repository finden Sie im [**pragma deleteclass**](pragma-deleteclass.md) -Präprozessorbefehl.

Die [com-API für WMI](com-api-for-wmi.md) verfügt über verschiedene Methoden zum Löschen einer Instanz und zum Löschen eines Objekts.

Im folgenden Verfahren wird beschrieben, wie Sie eine Basisklasse oder eine abgeleitete Klasse löschen.

**So löschen Sie eine Basisklasse oder eine abgeleitete Klasse**

-   Entweder die [**IWbemServices::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) -oder [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) -Methode aufrufen.

    Wie der Name vermuten lässt, löscht [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) eine Instanz asynchron, während [**deleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) eine Instanz synchron löscht. Um **DeleteClassAsync** verwenden zu können, müssen Sie auch ein [**iwbe"iwbejebjectsink**](iwbemobjectsink.md) "-Objekt implementieren.

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

 

 



