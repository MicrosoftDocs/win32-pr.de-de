---
title: MIDL-Compileroptionen
description: MIDL-Compileroptionen
ms.assetid: a78505cf-cda6-4b41-abd1-2609aec4dcb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649cd96ffc0afa171ad218a737910ce15facbe0e9b5ef302dedb6615228bcf3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859330"
---
# <a name="midl-compiler-options"></a>MIDL-Compileroptionen

Sie können die folgenden Befehlszeilenoptionen verwenden, um ein Gewisses des Standardverhaltens des MIDL-Compilers außer Kraft zu setzen und Optimierungen auszuwählen, die für Ihre Anwendung geeignet sind. Eine vollständige Liste der MIDL-Befehlszeilenoptionen finden Sie in der [MIDL-Command-Line Referenz.](/windows/desktop/Midl/midl-command-line-reference)



| Befehlszeilenschalter                                       | Beschreibung                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**/acf**](/windows/desktop/Midl/-acf)<br/>                          | Verwenden Sie , um einen expliziten ACF-Dateinamen zur Verfügung zu stellen. Dieser Schalter ermöglicht auch die Verwendung verschiedener Schnittstellennamen in den IDL- und ACF-Dateien.<br/>                                                                                                       |
| [**/dlldata**](/windows/desktop/Midl/-dlldata)<br/>                  | Gibt einen Dateinamen für die generierte DLL-Datendatei für eine Proxy-DLL an. Der Standarddateiname lautet Dlldata.c.<br/>                                                                                                                              |
| [**/env**](/windows/desktop/Midl/-env)<br/>                          | Weist MIDL an, Stubs oder eine Typbibliothek für eine Zielumgebung zu generieren.<br/>                                                                                                                                                            |
| [**/header**](/windows/desktop/Midl/-header), [ **/h**](/windows/desktop/Midl/-h)<br/> | Gibt den Namen der Schnittstellenheaderdatei an. Der Standardname ist der der IDL-Datei mit der Erweiterung .h.<br/>                                                                                                                       |
| [**/iid**](/windows/desktop/Midl/-iid)<br/>                          | Gibt einen Dateinamen für den Schnittstellenbezeichner an, der den Dateinamen des Standardschnittstellenbezeichners für eine COM-Schnittstelle überschreibt.<br/>                                                                                                              |
| [**/lcid**](/windows/desktop/Midl/-lcid)<br/>                        | Bietet vollständige DBCS-Unterstützung, sodass Sie internationale Zeichen in Ihren Eingabedateien, Dateinamen und Verzeichnispfaden verwenden können.<br/>                                                                                                          |
| [**/no \_ format \_ opt**](/windows/desktop/Midl/-no-format-opt)<br/>    | Um die Codegröße zu reduzieren, entfernt MIDL standardmäßig doppelte Deskriptoren. Dieser Schalter deaktiviert dieses Optimierungsverhalten.<br/>                                                                                                               |
| [**/Oi,**](/windows/desktop/Midl/-oi) **/Oic,** **/Oif**<br/>        | Weist MIDL an, eine vollständig interpretierte Marshallingmethode zu verwenden. Die Schalter /Oic und /Oicf bieten zusätzliche Leistungsverbesserungen.<br/>                                                                                                   |
| [**/out**](/windows/desktop/Midl/-out)<br/>                          | Gibt das Verzeichnis an, in das der MIDL-Compiler Ausgabedateien schreibt. Das Ausgabeverzeichnis kann mit einem Laufwerkbuchstaben, einem absoluten Pfadnamen oder beidem angegeben werden. Der Standardwert ist, dass MIDL die Dateien in das aktuelle Verzeichnis schreibt.<br/> |
| [**/proxy**](/windows/desktop/Midl/-proxy)<br/>                      | Gibt den Namen für die Schnittstellen-Proxydatei für die COM-Schnittstelle an. Der Standardname ist der der IDL-Datei plus " \_ p.c".<br/>                                                                                                            |
| [**/tlb**](/windows/desktop/Midl/-tlb)<br/>                          | Gibt den Namen der Typbibliotheksdatei an. Der Standardname ist der der IDL-Datei mit der Erweiterung TLB.<br/>                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MIDL-Kompilierung](midl-compilation.md)
</dt> </dl>

 

