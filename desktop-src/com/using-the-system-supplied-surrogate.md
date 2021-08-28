---
title: Verwenden des System-Supplied Ersatzzeichens
description: Verwenden des System-Supplied Ersatzzeichens
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0faec7c57f0e2010d0e817a4e44b81d65ad207371b591296bea2354307c7b80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119243430"
---
# <a name="using-the-system-supplied-surrogate"></a>Verwenden des System-Supplied Ersatzzeichens

Um das vom System bereitgestellte Ersatzzeichen für Ihren DLL-Server zu verwenden, registrieren Sie die DLL, indem Sie eine leere Zeichenfolge oder **NULL** für den [DllSurrogate-Wert](dllsurrogate.md) in der Registrierung angeben. Wenn eine Aktivierungsanforderung für einen DLL-Server, der so festgelegt ist, an COM gesendet wird, startet COM gleichzeitig den Standard-Ersatzprozess und die angeforderte DLL (indem die CLSID intern in der Startbefehlszeile angegeben wird), um einen separaten Aufruf zu vermeiden. (Informationen zum Ausführen mehrerer DLL-Server in einem Ersatzprozess finden Sie unter [Ersatzzeichenfreigabe](surrogate-sharing.md).)

Die Standardimplementierung des Ersatzzeichenprozesses ist ein Pseudo-COM-Server im Mixed Threading-Modellstil. Wenn mehrere DLL-Server in einen einzelnen Ersatzprozess geladen werden, stellt dieser Prozess sicher, dass jeder DLL-Server mithilfe des threadingmodells instanziiert wird, das in der Registrierung für diesen Server angegeben ist. Alle geladenen Freethreadserver befinden sich zusammen im Multithread-Apartment, während sich jeder Apartmentthreadserver in einem Singlethread-Apartment befindet. Wenn ein DLL-Server beide Threadingmodelle unterstützt, wählt COM Multithreading aus.

Dieser Ersatzprozess wird so geschrieben, dass COM sowohl das Entladen von DLL-Servern als auch das Beenden des Ersatzprozesses verarbeitet.

Das vom System bereitgestellte Ersatzzeichen funktioniert für die meisten Entwickler sehr gut und ist sehr einfach zu verwenden. Entwickler mit besonderen Überlegungen können jedoch entscheiden, dass ein benutzerdefiniertes Ersatzzeichen erforderlich ist. Weitere Informationen finden Sie unter [Schreiben eines benutzerdefinierten Ersatzzeichens.](writing-a-custom-surrogate.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DLL-Ersatzzeichen](dll-surrogates.md)
</dt> </dl>

 

 




