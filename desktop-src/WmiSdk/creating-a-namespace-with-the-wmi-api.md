---
description: Eine weitere Möglichkeit zum Erstellen eines Namespace ist die Verwendung der WMI-API, um den Namespace programmgesteuert zu erstellen.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Erstellen eines Namespace mit der WMI-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192bb38b60c3d0ddefb8cc1e5cb7b5f78cb0f5ba7937d39784729e0f61f70b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612540"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Erstellen eines Namespace mit der WMI-API

Eine weitere Möglichkeit zum Erstellen eines Namespace ist die Verwendung der WMI-API, um den Namespace programmgesteuert zu erstellen. Der Vorteil der programmgesteuerten Erstellung eines Namespace ist, dass Sie den Namespace aus einer Anwendung erstellen können. Die Verwendung der WMI-API ist jedoch komplexer als die Verwendung von MOF-Code (Managed Object Format), und Sie können Ihre Namespaces nicht so einfach für andere Entwickler freigeben.

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe der WMI-API einen Namespace erstellen.

**So erstellen Sie einen Namespace mithilfe der WMI-API**

1.  Verwenden [**Sie IWbemServices::GetObject,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) um einen Zeiger auf ein [**IWbemClassObject-Objekt**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) abzurufen, das auf die [**\_ \_ Namespace-Systemklasse**](--namespace.md) zeigt.
2.  Definieren Sie eine Instanz der [**\_ \_ Namespace-Systemklasse**](--namespace.md) mit einem Aufruf von [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  Legen Sie **die Name-Eigenschaft** der [**\_ \_ Namespace-Instanz**](--namespace.md) mit einem Aufruf von [**IWbemClassObject::P ut fest.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
4.  Erstellen Sie den Namespace mit einem Aufruf von [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    Der *pInst-Parameter* [**von PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) sollte auf die neue Instanz verweisen.

 

 



