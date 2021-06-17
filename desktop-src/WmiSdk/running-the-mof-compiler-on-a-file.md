---
description: 'Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: das Befehlszeilenprogramm oder eine programmgesteuerte Schnittstelle.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Ausführen des MOF-Compilers für eine Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230244"
---
# <a name="running-the-mof-compiler-on-a-file"></a>Ausführen des MOF-Compilers für eine Datei

Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: das Befehlszeilenprogramm oder eine programmgesteuerte Schnittstelle.

Bis Sie den MOF-Compiler [**Mofcomp.exe**](mofcomp.md)ausführen, ist ein Anbieter nicht bei WMI registriert, und die klassen, die er in der MOF-Datei erstellt hat, sind im [*WMI-Repository*](gloss-w.md)nicht verfügbar. Im folgenden Verfahren wird beschrieben, wie Sie eine MOF-Datei kompilieren.

**So führen Sie den MOF-Compiler in einer Datei über die Befehlszeile aus**

1.  Rufen Sie den MOF-Compiler über die Befehlszeile mit der folgenden Syntax auf.

    **mofcomp** _MOFfile_**.mof**

    Der MOF-Compiler unterstützt eine Vielzahl von Schaltern, um spezielle Verarbeitungssituationen zu steuern. Alle Switches sind optional, und jede Kombination von Schaltern ist zulässig. Es ist jedoch nicht sinnvoll, einige der Schalter in Kombination mit anderen zu verwenden. Wenn sie beispielsweise die Schalter **-class:updateonly** und **-class:createonly kombinieren,** führt dies dazu, dass der Compiler keine Aktion ausführt.

    Standardmäßig speichert Mofcomp.exe die kompilierten Klassen im \\ WMI-Stammnamespace. Beachten Sie, dass der Standardnamespace für Mofcomp.exe nicht mit dem Standardnamespace für die Skripterstellung identisch ist. Der Standardnamespace für die Skripterstellung wird im WMI-Steuerelement auf der Registerkarte Erweitert angegeben. Weitere Informationen finden Sie unter [Festlegen der Namespacesicherheit mit dem WMI-Steuerelement](setting-namespace-security-with-the-wmi-control.md).

    Sie können den Namespace, der die Klassen empfängt, auf zwei Arten ändern.

    1.  Verwenden Sie den Schalter **-N** für den **mofcomp-Befehl.**
    2.  Fügen Sie den \# [**Präprozessorbefehls-Pragmanamespace**](pragma-namespace.md) in die MOF-Datei ein.

2.  Optional können Sie eine MOF-Datei programmgesteuert kompilieren. Weitere Informationen finden Sie unter [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompilieren von MOF-Dateien](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 



