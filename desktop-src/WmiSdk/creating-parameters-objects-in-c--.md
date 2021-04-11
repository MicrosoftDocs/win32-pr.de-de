---
description: 'Die IWbemServices:: ExecMethod-Methode oder die ExecMethodAsync-Methode erfordert die \_ \_ Parameters-System Klasse als Container in pinparams, wenn die Methode, die Sie ausführen, über Eingabeargumente verfügt.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Erstellen von Parameter Objekten in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215459"
---
# <a name="creating-parameters-objects-in-c"></a>Erstellen von Parameter Objekten in C++

Die [**IWbemServices:: ExecMethod-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) oder die [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) -Methode erfordert die [**\_ \_ Parameters**](--parameters.md) -System Klasse als Container in *pinparams* , wenn die Methode, die Sie ausführen, über Eingabeargumente verfügt.

Im folgenden Verfahren wird beschrieben, wie eine Instanz der [**\_ \_ para**](--parameters.md) meters-System Klasse zum Speichern von Parameterinformationen erstellt wird.

**So erstellen Sie eine Instanz von \_ \_ Parametern**

1.  Bestimmen Sie den Klassenpfad für die Klasse, die die Methoden Definition enthält.
2.  Verwenden Sie den Klassenpfad und den von [**iwbemproviderinit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)übergebenen [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger [**, um die**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) Eingabe-und Ausgabeparameter Klassen abzurufen.

    Die [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) -Methode gibt einen [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger für den Zugriff auf jede dieser Klassen zurück.

3.  Verwenden Sie den [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Zeiger für die Output-Klasse, um eine Instanz der- [**Klasse zu erstellen**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .
4.  Füllen Sie die-Klasseninstanz aus, indem Sie die Eigenschaften festlegen, die den Ausgabe Werten entsprechen, und, wenn ein Rückgabewert für die-Methode vorhanden ist, die [ReturnValue](creating-a-method.md) -Eigenschaft.
5.  Übergeben Sie die [**\_ \_ Parameter**](--parameters.md) Instanz über die [**iwbemubjectsink::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) Expression-Methode an den Aufrufer zurück.

Nachdem ein Methoden Anbieter festgestellt hat, dass die Eingabeparameter korrekt sind, kann die Methode, auf die von " *strinmethodname* " verwiesen wird, trotzdem bestehen oder fehlschlagen Einige Methoden Anbieter erzeugen einen zweiten Thread, um die-Methode zu implementieren, sodass der tatsächliche Erfolg oder Fehler der Methode dem Aufrufer über [**iwbemubjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)gemeldet wird. Beachten Sie, dass " **iwbemubjectsink:: SetStatus** " nicht den Rückgabecode der Anbieter Methode empfängt. Er empfängt jedoch den Rückgabecode des eigentlichen Rückrufmechanismus und ist nur nützlich, um zu überprüfen, ob der-Befehl aufgetreten ist, oder dass er aus mechanischen Gründen fehlgeschlagen ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> <dt>

[**Iwbemcallresult:: getresultobject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



