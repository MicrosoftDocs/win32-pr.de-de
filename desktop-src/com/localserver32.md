---
title: LocalServer32
description: Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- LocalServer32 Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517165"
---
# <a name="localserver32"></a>LocalServer32

Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a>Bemerkungen

Der **serverausführ Bare** Wert, der vom Typ **reg \_ SZ** ist und ab Windows Server 2003 unterstützt wird, kann zusammen [**mit dem unter**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) Schlüssel **LocalServer32** verwendet werden, um Mehrdeutigkeiten bei der Verwendung der Funktion "-Funktion" zu vermeiden. **LocalServer32** gibt den Speicherort der zu startenden COM-Serveranwendung an. diese Informationen werden als erster Parameter *lpApplicationName* für " **feateprocess**" übergeben. Abhängig von der Implementierung von " **kreateprocess**" sind diese Informationen möglicherweise mehrdeutig. Wenn **serverausführ Bare Datei** angegeben wird, übergibt com den benannten Wert **serverexe** an den *lpApplicationName* -Parameter von " **kreateprocess**". Wenn **serverexe** nicht angegeben wird, übergibt com **null** als Wert für den ersten Parameter von " **kreateprocess**".

Um die Systemsicherheit bereitzustellen, verwenden Sie Zeichen folgen in Anführungszeichen im Pfad, um anzugeben, wo der ausführbare Dateiname endet und die Argumente beginnen. Anstatt z. b. den folgenden Pfad als **LocalServer32** -Eintrag anzugeben:

"C: \\ Programmdateien- \\ Unternehmens Dateien \\Application.exe param1 Param2"

Geben Sie den Pfad mit der folgenden Syntax an:

" \\ C: \\ Programmdateien- \\ Unternehmens Dateien \\Application.exe\\ " Param1 Param2 "

COM fügt das Flag "-Einbettungs" an die Zeichenfolge an, sodass die Anwendung, die Flags verwendet, die gesamte Zeichenfolge analysieren und nach dem-Einbettungs Flag suchen muss.

Wenn com einen lokalen 32-Bit-Server startet, muss der Server ein Klassenobjekt innerhalb einer vom Benutzer festgelegten Zeit registrieren. Der Wert für die verstrichene Zeit muss standardmäßig mindestens 5 Minuten betragen (in Millisekunden), kann jedoch die Anzahl der Millisekunden in 30 Tagen nicht überschreiten. Anwendungen sollten diesen Wert in der Regel nicht festlegen, der im Eintrag **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ COM2 \\ serverstartelapsedtime** aufgeführt ist.

Die erforderlichen Einträge für lokale 32-Bit-Server sind [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** und [**Insertable**](insertable.md).

Wenn ein Container die Registrierung nach einem lokalen Server durchsucht, hat ein lokaler 32-Bit-Server Vorrang vor einem 16-Bit-lokalen Server.

Wenn Sie Klassen als Dienste implementieren, sollten Sie beachten, dass der benannte Wert " [**LocalService**](localservice.md) " bevorzugt für den **LocalServer32** -Schlüssel für lokale und Remote Aktivierungs Anforderungen verwendet wird. wenn " **LocalService** " vorhanden ist und sich auf einen gültigen Dienst bezieht, wird die **LocalServer32** -Taste ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**LocalServer**](localserver.md)
</dt> <dt>

[**LocalService**](localservice.md)
</dt> </dl>

 

 