---
description: 'Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: mithilfe des Befehlszeilen-Hilfsprogramms oder mithilfe einer programmgesteuerten Schnittstelle.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Ausführen des MOF-Compilers für eine Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1605544e05f59670f9e6fd73fcd8c01862b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215336"
---
# <a name="running-the-mof-compiler-on-a-file"></a>Ausführen des MOF-Compilers für eine Datei

Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: mithilfe des Befehlszeilen-Hilfsprogramms oder mithilfe einer programmgesteuerten Schnittstelle.

Wenn Sie den MOF-Compiler [**Mofcomp.exe**](mofcomp.md)ausführen, ist ein Anbieter nicht bei WMI registriert, und die in der MOF-Datei erstellten Klassen sind im [*WMI-Repository*](gloss-w.md)nicht verfügbar. Im folgenden Verfahren wird beschrieben, wie eine MOF-Datei kompiliert wird.

**So führen Sie den MOF-Compiler für eine Datei in der Befehlszeile aus**

1.  Verwenden Sie die folgende Syntax, um den MOF-Compiler von der Befehlszeile aus aufzurufen.

    **MAF Comp** -Datei ** * *. MOF**

    Der MOF-Compiler unterstützt eine Vielzahl von Schaltern, um besondere Verarbeitungs Situationen zu steuern. Alle Schalter sind optional, und eine beliebige Kombination von Switches ist zulässig. Es ist jedoch nicht sinnvoll, einige Switches in Kombination mit anderen Switches zu verwenden. Wenn Sie z. b. die Schalter **-Class: updateonly** und **-Class:** |.

    Standardmäßig speichert Mofcomp.exe die kompilierten Klassen im standardmäßigen \\ WMI-Standard Namespace. Beachten Sie, dass der Standard Namespace für Mofcomp.exe nicht mit dem Standard Namespace für die Skripterstellung identisch ist. Der Standard Namespace für die Skripterstellung wird im WMI-Steuerelement auf der Registerkarte Erweitert angegeben. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.

    Sie können den Namespace, der die Klassen empfängt, auf zwei Arten ändern.

    1.  Verwenden Sie den Schalter **-N** für den Befehl " **MUF Comp** ".
    2.  Fügen Sie den \# [**pragma-Namespace**](pragma-namespace.md) des Präprozessorbefehls in die MOF-Datei ein.

2.  Optional können Sie eine MOF-Datei Programm gesteuert kompilieren. Weitere Informationen finden Sie unter [**imuf Compiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompilieren von MOF-Dateien](compiling-mof-files.md)
</dt> <dt>

[**Mofcomp**](mofcomp.md)
</dt> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 



