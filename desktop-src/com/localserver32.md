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
# <a name="localserver32"></a><span data-ttu-id="48b36-104">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="48b36-104">LocalServer32</span></span>

<span data-ttu-id="48b36-105">Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.</span><span class="sxs-lookup"><span data-stu-id="48b36-105">Specifies the full path to a 32-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="48b36-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="48b36-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a><span data-ttu-id="48b36-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48b36-107">Remarks</span></span>

<span data-ttu-id="48b36-108">Der **serverausführ Bare** Wert, der vom Typ **reg \_ SZ** ist und ab Windows Server 2003 unterstützt wird, kann zusammen [**mit dem unter**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) Schlüssel **LocalServer32** verwendet werden, um Mehrdeutigkeiten bei der Verwendung der Funktion "-Funktion" zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="48b36-108">The **ServerExecutable** value, which is of type **REG\_SZ** and is supported starting with Windows Server 2003, works in conjunction with the **LocalServer32** subkey to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="48b36-109">**LocalServer32** gibt den Speicherort der zu startenden COM-Serveranwendung an. diese Informationen werden als erster Parameter *lpApplicationName* für " **feateprocess**" übergeben.</span><span class="sxs-lookup"><span data-stu-id="48b36-109">**LocalServer32** specifies the location of the COM server application to launch, and this information is passed as the first parameter *lpApplicationName* for **CreateProcess**.</span></span> <span data-ttu-id="48b36-110">Abhängig von der Implementierung von " **kreateprocess**" sind diese Informationen möglicherweise mehrdeutig.</span><span class="sxs-lookup"><span data-stu-id="48b36-110">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="48b36-111">Wenn **serverausführ Bare Datei** angegeben wird, übergibt com den benannten Wert **serverexe** an den *lpApplicationName* -Parameter von " **kreateprocess**".</span><span class="sxs-lookup"><span data-stu-id="48b36-111">For this reason, if **ServerExecutable** is specified, COM passes the **ServerExecutable** named value to the *lpApplicationName* parameter of **CreateProcess**.</span></span> <span data-ttu-id="48b36-112">Wenn **serverexe** nicht angegeben wird, übergibt com **null** als Wert für den ersten Parameter von " **kreateprocess**".</span><span class="sxs-lookup"><span data-stu-id="48b36-112">If **ServerExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

<span data-ttu-id="48b36-113">Um die Systemsicherheit bereitzustellen, verwenden Sie Zeichen folgen in Anführungszeichen im Pfad, um anzugeben, wo der ausführbare Dateiname endet und die Argumente beginnen.</span><span class="sxs-lookup"><span data-stu-id="48b36-113">To help provide system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="48b36-114">Anstatt z. b. den folgenden Pfad als **LocalServer32** -Eintrag anzugeben:</span><span class="sxs-lookup"><span data-stu-id="48b36-114">For example, instead of specifying the following path as the **LocalServer32** entry:</span></span>

<span data-ttu-id="48b36-115">"C: \\ Programmdateien- \\ Unternehmens Dateien \\Application.exe param1 Param2"</span><span class="sxs-lookup"><span data-stu-id="48b36-115">"C:\\Program Files\\Company Files\\Application.exe param1 param2"</span></span>

<span data-ttu-id="48b36-116">Geben Sie den Pfad mit der folgenden Syntax an:</span><span class="sxs-lookup"><span data-stu-id="48b36-116">specify the path using the following syntax:</span></span>

<span data-ttu-id="48b36-117">" \\ C: \\ Programmdateien- \\ Unternehmens Dateien \\Application.exe\\ " Param1 Param2 "</span><span class="sxs-lookup"><span data-stu-id="48b36-117">"\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2"</span></span>

<span data-ttu-id="48b36-118">COM fügt das Flag "-Einbettungs" an die Zeichenfolge an, sodass die Anwendung, die Flags verwendet, die gesamte Zeichenfolge analysieren und nach dem-Einbettungs Flag suchen muss.</span><span class="sxs-lookup"><span data-stu-id="48b36-118">COM appends the "-Embedding" flag to the string, so the application that uses flags needs to parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="48b36-119">Wenn com einen lokalen 32-Bit-Server startet, muss der Server ein Klassenobjekt innerhalb einer vom Benutzer festgelegten Zeit registrieren.</span><span class="sxs-lookup"><span data-stu-id="48b36-119">When COM starts a 32-bit local server, the server must register a class object within an elapsed time set by the user.</span></span> <span data-ttu-id="48b36-120">Der Wert für die verstrichene Zeit muss standardmäßig mindestens 5 Minuten betragen (in Millisekunden), kann jedoch die Anzahl der Millisekunden in 30 Tagen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="48b36-120">By default, the elapsed time value must be at least 5 minutes, in milliseconds, but cannot exceed the number of milliseconds in 30 days.</span></span> <span data-ttu-id="48b36-121">Anwendungen sollten diesen Wert in der Regel nicht festlegen, der im Eintrag **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ COM2 \\ serverstartelapsedtime** aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="48b36-121">Applications typically should not set this value, which is in the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\COM2\\ServerStartElapsedTime** entry.</span></span>

<span data-ttu-id="48b36-122">Die erforderlichen Einträge für lokale 32-Bit-Server sind [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** und [**Insertable**](insertable.md).</span><span class="sxs-lookup"><span data-stu-id="48b36-122">The required entries for 32-bit local servers are [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32**, and [**Insertable**](insertable.md).</span></span>

<span data-ttu-id="48b36-123">Wenn ein Container die Registrierung nach einem lokalen Server durchsucht, hat ein lokaler 32-Bit-Server Vorrang vor einem 16-Bit-lokalen Server.</span><span class="sxs-lookup"><span data-stu-id="48b36-123">If a container is searching the registry for a local server, a 32-bit local server has priority over a 16-bit local server.</span></span>

<span data-ttu-id="48b36-124">Wenn Sie Klassen als Dienste implementieren, sollten Sie beachten, dass der benannte Wert " [**LocalService**](localservice.md) " bevorzugt für den **LocalServer32** -Schlüssel für lokale und Remote Aktivierungs Anforderungen verwendet wird. wenn " **LocalService** " vorhanden ist und sich auf einen gültigen Dienst bezieht, wird die **LocalServer32** -Taste ignoriert.</span><span class="sxs-lookup"><span data-stu-id="48b36-124">If you are implementing classes as services, you should be aware that the [**LocalService**](localservice.md) named value is used in preference to the **LocalServer32** key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48b36-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48b36-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48b36-126">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="48b36-126">**LocalServer**</span></span>](localserver.md)
</dt> <dt>

[<span data-ttu-id="48b36-127">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="48b36-127">**LocalService**</span></span>](localservice.md)
</dt> </dl>

 

 