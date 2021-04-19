---
description: Beschreibt den Prozess des erbauens einer WSDAPI-Anwendung mithilfe von wsdcodegen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Verwenden von wsdcodegen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e09bd2b0c8f96d51751aa90bc3206a0824f19b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350247"
---
# <a name="using-wsdcodegen"></a>Verwenden von wsdcodegen

**So erstellen Sie eine WSDAPI-Anwendung mithilfe von wsdcodegen**

1.  Definieren Sie den funktionalen Vertrag für den Geräte Host in einer WSDL-Datei.
2.  Generieren Sie eine Konfigurationsdatei mithilfe von wsdcodegen. Weitere Informationen finden Sie unter [wsdcodegen-Konfigurationsdatei](wsdcodegen-configuration-file.md) und [Befehlszeilen Syntax von wsdcodegen](wsdcodegen-command-line-syntax.md).
3.  Öffnen Sie die generierte Konfigurationsdatei, und ändern Sie die Datei nach Bedarf. Wenn Sie eine Client Anwendung entwickeln, sind nur wenige oder gar keine Änderungen erforderlich. Wenn Sie eine Host Anwendung entwickeln, ändern Sie die benutzerspezifischen Konfigurationselemente (z. b. [**Hersteller**](manufacturer.md) und [**modelname**](modelname.md)).
4.  Generieren Sie mithilfe von wsdcodegen Code, und geben Sie die Konfigurationsdatei als Eingabe an. Weitere Informationen finden Sie unter [Befehlszeilen Syntax von wsdcodegen](wsdcodegen-command-line-syntax.md).
5.  Verwenden Sie den generierten Code zum Erstellen eines Clients, Hosts oder beides.

Die Windows SDK umfasst einige WSDL-Beispieldateien, wsdcodegen-Konfigurationsdateien und generierten Code. Weitere Informationen finden Sie unter [WSDAPI Samples](wsdapi-samples.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Beispiele](wsdapi-samples.md)
</dt> </dl>

 

 



