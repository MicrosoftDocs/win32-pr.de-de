---
description: Im Gegensatz zum Löschen einer dynamischen Instanz ist das Löschen einer Klasse eine einfache Prozedur.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Löschen einer Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad3e44292aa1ca6b534151a82f36df50802e04db788d8cfb8aaeb477c23164f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412090"
---
# <a name="deleting-a-class"></a>Löschen einer Klasse

Im Gegensatz zum Löschen einer dynamischen Instanz ist das Löschen einer Klasse eine einfache Prozedur. Wie bereits erwähnt, werden Basisklassen oder abgeleitete Klassen jedoch nur selten gelöscht. Stattdessen wird eine -Instanz häufiger gelöscht. Die [Skripterstellungs-API für WMI](scripting-api-for-wmi.md) verwendet die gleichen Methoden, um entweder ein Klassenobjekt oder eine Instanz zu löschen. Weitere Informationen finden Sie unter [Löschen einer Instanz.](deleting-an-instance.md) Informationen zum Entfernen von Klassen und Instanzen aus dem WMI-Repository finden Sie im [**Pragma deleteclass-Präprozessorbefehl.**](pragma-deleteclass.md)

Die [COM-API für WMI](com-api-for-wmi.md) verfügt über verschiedene Methoden zum Löschen einer Instanz und zum Löschen eines Objekts.

Im folgenden Verfahren wird beschrieben, wie eine Basisklasse oder abgeleitete Klasse gelöscht wird.

**So löschen Sie eine Basisklasse oder abgeleitete Klasse**

-   Rufen Sie entweder die [**Methode IWbemServices::D eleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) oder [**IWbemServices::D eleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) auf.

    Wie der Name schon sagt, löscht [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) eine Instanz asynchron, während [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) eine Instanz synchron löscht. Um **DeleteClassAsync** zu verwenden, müssen Sie auch ein [**IWbemObjectSink-Objekt**](iwbemobjectsink.md) implementieren.

> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf der gleichen Authentifizierungsebene zurückgegeben wird, die der Client erfordert, wird empfohlen, anstelle der asynchronen Kommunikation semisynchron zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

 

 



