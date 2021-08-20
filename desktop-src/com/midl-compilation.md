---
title: MIDL-Kompilierung
description: MIDL-Kompilierung
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a94f94122aeeb1f2900c3adec7e567c794f31ee22259f657dfe5e95f3f688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047948"
---
# <a name="midl-compilation"></a>MIDL-Kompilierung

Bei einer IDL-Datei wie [Example2.idl,](anatomy-of-an-idl-file.md)die eine oder mehrere COM-Schnittstellen und eine Typbibliothek definiert, generiert der MIDL-Compiler (Midl.exe) die in der folgenden Tabelle beschriebenen Dateien als Standardausgabe.



| Dateiname                 | BESCHREIBUNG                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Example2.h<br/>    | Die Headerdatei, die Typdefinitionen und Funktionsdeklarationen für alle schnittstellen enthält, die in der IDL-Datei definiert sind, sowie Vorwärtsdeklarationen für Routinen, die die Stubs aufrufen.<br/> |
| Beispiel2 \_ p.c<br/> | Die Proxy-/Stubdatei, die die Ersatzeinstiegspunkte sowohl für Clients als auch für Server enthält.<br/>                                                                                           |
| Example2 \_ i.c<br/> | Die Schnittstellen-ID-Datei, die die GUID für jede schnittstelle definiert, die in der IDL-Datei angegeben ist.<br/>                                                                                               |
| Example2.tlb<br/>  | Eine zusammengesetzte Dokumentdatei, die Informationen zu Typen und Objekten enthält.<br/>                                                                                                                |
| Dlldata.c<br/>     | Enthält die Daten, die Sie zum Erstellen einer Proxy-/Stub-DLL benötigen.<br/>                                                                                                                                     |



 

Sie verwenden die Headerdatei und alle C-Dateien, um [eine Proxy-DLL](building-and-registering-a-proxy-dll.md) zu erstellen, die die -Schnittstelle unterstützen kann, wenn sie sowohl von Clientanwendungen als auch von Objektservern verwendet wird. Sie verwenden die Schnittstellenheaderdatei (Example2.h) und die Schnittstellen-ID (Example2 \_ i.c), wenn Sie die ausführbare Datei für eine Clientanwendung erstellen, die die -Schnittstelle verwendet. Sie können die Typbibliotheksdatei als Ressource in Ihre EXE- oder DLL-Datei einschließen oder als separate Datei versenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Für eine COM-Schnittstelle generierte Dateien](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[MIDL-Compileroptionen](midl-compiler-options.md)
</dt> </dl>

 

