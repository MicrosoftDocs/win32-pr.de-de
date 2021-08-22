---
description: 'Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: die Verwendung des Befehlszeilenprogramms oder die Verwendung einer programmgesteuerten Schnittstelle.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Ausführen des MOF-Compilers für eine Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a70c32e82b826f2ab02403e7e269e711704d826ad4b4f9465638df0b0745f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050328"
---
# <a name="running-the-mof-compiler-on-a-file"></a>Ausführen des MOF-Compilers für eine Datei

Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: die Verwendung des Befehlszeilenprogramms oder die Verwendung einer programmgesteuerten Schnittstelle.

Bis Sie den MOF-Compiler [**Mofcomp.exe**](mofcomp.md)ausführen, ist ein Anbieter nicht bei WMI registriert, und die klassen, die er in der MOF-Datei erstellt hat, sind im [*WMI-Repository nicht verfügbar.*](gloss-w.md) Im folgenden Verfahren wird beschrieben, wie Sie eine MOF-Datei kompilieren.

**So führen Sie den MOF-Compiler in einer Datei über die Befehlszeile aus**

1.  Rufen Sie den MOF-Compiler mithilfe der folgenden Syntax über die Befehlszeile auf.

    **mofcomp** _MOFfile_**.mof**

    Der MOF-Compiler unterstützt eine Vielzahl von Schaltern, um spezielle Verarbeitungssituationen zu steuern. Alle Schalter sind optional, und eine beliebige Kombination von Switches ist zulässig. Es ist jedoch nicht sinnvoll, einige der Switches in Kombination mit anderen zu verwenden. Wenn Sie beispielsweise die Schalter **-class:updateonly** und **-class:createonly** kombinieren, führt dies dazu, dass der Compiler keine Aktion führt.

    Standardmäßig speichert Mofcomp.exe die kompilierten Klassen im \\ WMI-Standardnamespace des Stamms. Beachten Sie, dass der Standardnamespace für Mofcomp.exe nicht mit dem Standardnamespace für die Skripterstellung identisch ist. Der Standardnamespace für die Skripterstellung wird im WMI-Steuerelement auf der Registerkarte Erweitert angegeben. Weitere Informationen finden Sie unter [Festlegen der Namespacesicherheit mit dem WMI-Steuerelement](setting-namespace-security-with-the-wmi-control.md).

    Sie können den Namespace, der die Klassen empfängt, auf zwei Arten ändern.

    1.  Verwenden Sie **den Schalter -N** für den **Befehl mofcomp.**
    2.  Fügen Sie den Pragmanamespace des \# [**Präprozessorbefehls**](pragma-namespace.md) in die MOF-Datei ein.

2.  Optional können Sie eine MOF-Datei programmgesteuert kompilieren. Weitere Informationen finden Sie unter [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompilieren von MOF-Dateien](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 



