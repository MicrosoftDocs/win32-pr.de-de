---
description: Die IWbemServices::ExecMethod- oder ExecMethodAsync-Methoden erfordern die \_ \_ PARAMETERS-Systemklasse als Container in pInParams, wenn die von ihnen ausgeführte Methode Eingabeargumente aufweist.
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Erstellen von Parameterobjekten in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa97753eab9554e402a91cfce72a6435d44298b6b68a83de96fd4beccd83bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244520"
---
# <a name="creating-parameters-objects-in-c"></a>Erstellen von Parameterobjekten in C++

Die [**IWbemServices::ExecMethod-**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) oder [**ExecMethodAsync-Methoden**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) erfordern die [**\_ \_ PARAMETERS-Systemklasse**](--parameters.md) als Container in *pInParams,* wenn die von ihnen ausgeführte Methode Eingabeargumente aufweist.

Das folgende Verfahren beschreibt das Erstellen einer Instanz der [**\_ \_ PARAMETERS-Systemklasse**](--parameters.md) zum Speichern von Parameterinformationen.

**So erstellen Sie eine Instanz von \_ \_ PARAMETERS**

1.  Bestimmen Sie den Klassenpfad für die Klasse, die die Methodendefinition enthält.
2.  Rufen Sie mithilfe des Klassenpfads und des [**IWbemServices-Zeigers,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) der von [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)übergeben wird, [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) auf, um die Eingabe- und Ausgabeparameterklassen abzurufen.

    Die [**GetMethod-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) gibt einen [**IWbemClassObject-Zeiger**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) für den Zugriff auf jede dieser Klassen zurück.

3.  Rufen Sie mithilfe des [**IWbemClassObject-Zeigers**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) für die Ausgabeklasse [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) auf, um eine Instanz der -Klasse zu erstellen.
4.  Füllen Sie die Klasseninstanz auf, indem Sie die Eigenschaften festlegen, die den Ausgabewerten entsprechen, und, wenn ein Rückgabewert für die Methode vorhanden ist, die [ReturnValue-Eigenschaft.](creating-a-method.md)
5.  Übergeben Sie die [**\_ \_ PARAMETERS-Instanz**](--parameters.md) über die [**IWbemObjectSink::Indicate-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) zurück an den Aufrufer.

Nachdem ein Methodenanbieter festgestellt hat, dass die Eingabeparameter korrekt sind, kann die Methode, auf die *strMethodName* verweist, weiterhin erfolgreich sein oder fehlschlagen. Einige Methodenanbieter führen einen zweiten Thread aus, um die Methode zu implementieren, sodass der tatsächliche Erfolg oder Fehler der Methode dem Aufrufer über [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)gemeldet wird. Beachten Sie, dass **IWbemObjectSink::SetStatus** nicht den Rückgabecode der Anbietermethode empfängt. Er empfängt jedoch den Rückgabecode des tatsächlichen Aufrufrückgabemechanismus und ist nur nützlich, um zu überprüfen, ob der Aufruf aufgetreten ist oder aus technischen Gründen fehlgeschlagen ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> <dt>

[**IWbemCallResult::GetResultObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



