---
description: Eine weitere Möglichkeit zum Erstellen eines Namespace besteht darin, die WMI-API zu verwenden, um den Namespace Programm gesteuert zu erstellen.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Erstellen eines Namespace mit der WMI-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348548"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Erstellen eines Namespace mit der WMI-API

Eine weitere Möglichkeit zum Erstellen eines Namespace besteht darin, die WMI-API zu verwenden, um den Namespace Programm gesteuert zu erstellen. Der Vorteil der programmgesteuerten Erstellung eines Namespace besteht darin, dass Sie den Namespace in einer Anwendung erstellen können. Allerdings ist die Verwendung der WMI-API komplexer als die Verwendung von MOF-Code (Managed Object Format), und Sie können Ihre Namespaces nicht so einfach für andere Entwickler freigeben.

Im folgenden Verfahren wird beschrieben, wie Sie einen Namespace mithilfe der WMI-API erstellen.

**So erstellen Sie einen Namespace mithilfe der WMI-API**

1.  Verwenden Sie [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) zum Abrufen eines Zeigers auf ein [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Objekt, das auf die Klasse [**\_ \_ Namespace**](--namespace.md) System verweist.
2.  Definieren Sie eine Instanz der [**\_ \_ Namespace**](--namespace.md) -System Klasse mit einem-Befehl, der [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)aufruft.
3.  Legen Sie die **Name** -Eigenschaft der [**\_ \_ Namespace**](--namespace.md) Instanz mit einem Befehl [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)fest.
4.  Erstellen Sie den Namespace mit einem [**callbemservices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)-Befehl.

    Der *pinst* -Parameter von [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) sollte auf die neue Instanz verweisen.

 

 



