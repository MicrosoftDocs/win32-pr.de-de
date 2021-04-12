---
description: Zusätzlich zu Klassen und Instanzen können Sie mithilfe von WMI eine Methode ändern. Der Hauptgrund, warum Sie eine Methode ändern möchten, ist, wenn Sie die Implementierung einer Methode in einem Anbieter geändert haben. Weitere Informationen finden Sie unterschreiben eines Methoden Anbieters.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Ändern einer Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393329"
---
# <a name="modifying-a-method"></a>Ändern einer Methode

Zusätzlich zu Klassen und Instanzen können Sie mithilfe von WMI eine Methode ändern. Der Hauptgrund, warum Sie eine Methode ändern möchten, ist, wenn Sie die Implementierung einer Methode in einem Anbieter geändert haben. Weitere Informationen finden Sie unter [Schreiben eines Methoden Anbieters](writing-a-method-provider.md).

Das Ändern einer Methode ist kein Vorgang, der im Skript ausgeführt werden kann.

Im folgenden Verfahren wird beschrieben, wie eine Methode Programm gesteuert geändert wird.

**So ändern Sie eine Methode Programm gesteuert**

1.  Rufen Sie die Klassendefinition mit einem-Befehl von [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)ab.

    Die zwei out-Parameter *ppinsignature* und *ppoutsignature* enthalten die in-Parameter-Klasse bzw. die Out-Parameter-Klasse. Der Rückgabewert wird in der Out-Parameter-Klasse als Eigenschaft gebündelt und sollte als " **ReturnValue**" benannt werden.

2.  Rufen Sie die Parameter mit den Aufrufen von [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)oder [**IWbemClassObject::D Elete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)ab, und ändern Sie Sie.
3.  Platzieren Sie die neue Version der Methode mithilfe eines Aufrufens von [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)wieder in der übergeordneten Klasse.

Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

 

 



