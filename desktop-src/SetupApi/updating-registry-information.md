---
description: Nachdem der Commit für die Warteschlange erfolgreich ausgeführt wurde, müssen Sie die Registrierungsinformationen für das Produkt aktualisieren, das Sie installieren.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Aktualisieren von Registrierungsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579ef64739bbe063d6fed19234a74b89b86b8b257793a1a26e83fd651256d189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683050"
---
# <a name="updating-registry-information"></a>Aktualisieren von Registrierungsinformationen

Nachdem der Commit für die Warteschlange erfolgreich ausgeführt wurde, müssen Sie die Registrierungsinformationen für das Produkt aktualisieren, das Sie installieren. Es wird empfohlen, vor dem Ändern der Registrierungsinformationen zu warten, bis alle erforderlichen Dateikopiervorgänge erfolgreich abgeschlossen wurden.

Eine Möglichkeit zum Aktualisieren der Registrierung besteht darin, [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) mit den angegebenen Flags SPINST \_ INIFILES, SPINST \_ REGISTRY oder SPINST \_ INI2REG aufzurufen. Diese Flags können in einem Aufruf von **SetupInstallFromInfSection** kombiniert werden.

Im folgenden Beispiel wird SPINST \_ ALL^SPINST \_ FILES verwendet, um anzugeben, dass die Funktion alle aufgelisteten Vorgänge außer Dateivorgängen verarbeiten soll. Da nur INI-, Registrierungs- und Dateivorgänge im Abschnitt **Installieren** aufgeführt sind, ist dies eine kurzformige Methode, mit der angegeben wird, dass die Funktion alle INI- und Registrierungsvorgänge verarbeiten soll.

Das folgende Beispiel zeigt, wie Registrierungsinformationen mithilfe der **SetupInstallFromINFSection-Funktion** installiert werden.

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

Im Beispiel ist *OwnerWindow* **NULL,** da nur Dateivorgänge Dialogfelder generieren und daher kein übergeordnetes Fenster benötigt wird. "MyInf" ist die INF-Datei, die den zu verarbeitenden Abschnitt enthält. Der Parameter "MySection" gibt den zu installierenden Abschnitt an. Die kombinierten Flags SPINST \_ ALL ^ SPINST \_ FILES geben an, welche Installationsvorgänge verarbeitet werden sollen, in diesem Fall alle Vorgänge mit Ausnahme von Dateivorgängen. Der Quellstammpfad wird als "A: \\ " angegeben.

Da keine Kopiervorgänge verarbeitet werden, werden die Parameter *CopyFlags,* *MsgHandler,* *Context,* *DeviceInfoSet* und *DeviceInfoData* nicht angegeben.

 

 



