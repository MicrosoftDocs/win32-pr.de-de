---
title: Mittel l-Compileroptionen
description: Mittel l-Compileroptionen
ms.assetid: a78505cf-cda6-4b41-abd1-2609aec4dcb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e219daa345ad3140b78db8fdfc3de1d28678120
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316563"
---
# <a name="midl-compiler-options"></a>Mittel l-Compileroptionen

Sie können die folgenden Befehlszeilenoptionen verwenden, um ein gewisses Standardverhalten des Mittelwert-Compilers zu überschreiben und Optimierungen auszuwählen, die für Ihre Anwendung geeignet sind. Eine vollständige Liste der mittleren Befehlszeilenoptionen finden Sie in der [Referenz zur Mittel l-Command-Line](/windows/desktop/Midl/midl-command-line-reference).



| Befehlszeilenschalter                                       | Beschreibung                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**/acf**](/windows/desktop/Midl/-acf)<br/>                          | Verwenden Sie, um einen expliziten ACF-Dateinamen anzugeben. Dieser Switch ermöglicht außerdem die Verwendung verschiedener Schnittstellennamen in den IDL-und ACF-Dateien.<br/>                                                                                                       |
| [**/dlldata**](/windows/desktop/Midl/-dlldata)<br/>                  | Gibt einen Dateinamen für die generierte DLL-Datendatei für eine Proxy-dll an. Der Standard Dateiname ist "dlldata. c".<br/>                                                                                                                              |
| [**/ENV**](/windows/desktop/Midl/-env)<br/>                          | Leitet die Mittel l zum Generieren von Stubdaten oder einer Typbibliothek für eine Zielumgebung.<br/>                                                                                                                                                            |
| [**/Header**](/windows/desktop/Midl/-header), [ **/h**](/windows/desktop/Midl/-h)<br/> | Gibt den Namen der Schnittstellen Header Datei an. Der Standardname ist der der IDL-Datei mit der Erweiterung ". h".<br/>                                                                                                                       |
| [**/IID**](/windows/desktop/Midl/-iid)<br/>                          | Gibt einen schnittstellenbezeichnerdateinamen an, der den Standard Dateiname für eine COM-Schnittstelle überschreibt<br/>                                                                                                              |
| [**/LCID**](/windows/desktop/Midl/-lcid)<br/>                        | Bietet vollständige DBCS-Unterstützung, sodass Sie internationale Zeichen in ihren Eingabedateien, Dateinamen und Verzeichnis Pfaden verwenden können.<br/>                                                                                                          |
| [**/No \_ Format \_ Opt**](/windows/desktop/Midl/-no-format-opt)<br/>    | In der Standardeinstellung werden doppelte Deskriptoren vermieden, um die Codegröße zu verringern. Dieser Schalter deaktiviert dieses Optimierungs Verhalten.<br/>                                                                                                               |
| [**/Oi**](/windows/desktop/Midl/-oi), **/OIC**, **/OIF**<br/>        | Leitet die Mittel l an die Verwendung einer vollständig interpretierten Marshallingmethode. Die Schalter/OIC und/Oicf bieten weitere Leistungsverbesserungen.<br/>                                                                                                   |
| [**/Out**](/windows/desktop/Midl/-out)<br/>                          | Gibt das Verzeichnis an, in das der Mittell-Compiler Ausgabedateien schreibt. Das Ausgabeverzeichnis kann mit einem Laufwerk Buchstaben, einem absoluten Pfadnamen oder beidem angegeben werden. Der Standardwert ist, dass die Dateien von der mittleren l in das aktuelle Verzeichnis geschrieben werden.<br/> |
| [**/Proxy**](/windows/desktop/Midl/-proxy)<br/>                      | Gibt den Namen für die Schnittstellen-Proxydatei für die COM-Schnittstelle an. Der Standardname ist der der IDL-Datei plus " \_ p. c".<br/>                                                                                                            |
| [**/TLB**](/windows/desktop/Midl/-tlb)<br/>                          | Gibt den Namen der Typbibliotheksdatei an. Der Standardname ist der der IDL-Datei mit der Erweiterung. tlb.<br/>                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompilierung in mittlerer l](midl-compilation.md)
</dt> </dl>

 

