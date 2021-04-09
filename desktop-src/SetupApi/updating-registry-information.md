---
description: Nachdem für die Warteschlange ein Commit erfolgreich ausgeführt wurde, müssen Sie die Registrierungsinformationen für das Produkt aktualisieren, das Sie installieren.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Aktualisieren von Registrierungsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960441"
---
# <a name="updating-registry-information"></a>Aktualisieren von Registrierungsinformationen

Nachdem für die Warteschlange ein Commit erfolgreich ausgeführt wurde, müssen Sie die Registrierungsinformationen für das Produkt aktualisieren, das Sie installieren. Es wird empfohlen, dass Sie warten, bis alle erforderlichen Datei Kopiervorgänge erfolgreich abgeschlossen wurden, bevor Sie Registrierungsinformationen ändern.

Eine Möglichkeit zum Aktualisieren der Registrierung besteht darin, [**setupinstallfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) mit den angegebenen spinst- \_ Dateien, spinst \_ Registry oder spinst \_ INI2REG Flags aufzurufen. Diese Flags können in einem Befehl von **setupinstallfrominfsection** kombiniert werden.

Im folgenden Beispiel wird spinst \_ all ^ spinst- \_ Dateien verwendet, um anzugeben, dass die-Funktion alle aufgelisteten Vorgänge mit Ausnahme von Datei Vorgängen verarbeiten soll. Da nur ini-, Registrierungs-und Datei Vorgänge im **Installations** Abschnitt aufgeführt sind, ist dies eine Kurzmethode, um anzugeben, dass die-Funktion alle ini-und Registrierungs Vorgänge verarbeiten soll.

Im folgenden Beispiel wird gezeigt, wie Registrierungsinformationen mithilfe der **setupinstallfrominfsection** -Funktion installiert werden.

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

Im Beispiel ist "Besitzer *Window* " **null** , da nur Datei Vorgänge Dialogfelder generieren und somit kein übergeordnetes Fenster benötigt wird. "Myinf" ist die INF-Datei, die den zu verarbeitenden Abschnitt enthält. Der Parameter "mySection" gibt den zu installierenden Abschnitt an. Die kombinierten Flags, spinst \_ alle ^ spinst- \_ Dateien, geben an, welche Installations Vorgänge verarbeitet werden sollen, in diesem Fall alle Vorgänge mit Ausnahme von Datei Vorgängen. Der Quell Stamm Pfad wird als "A: \\ " angegeben.

Da keine Kopiervorgänge verarbeitet werden, werden die Parameter " *copyflags*", " *msghandler*", " *context*", " *deviceinfoset*" und " *deviceinfodata* " nicht angegeben.

 

 



