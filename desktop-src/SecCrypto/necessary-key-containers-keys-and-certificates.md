---
description: Die Beispiel Programme in den folgenden Abschnitten führen Vorgänge aus, die erfordern, dass öffentliche/private Schlüsselpaare zum Verschlüsseln und Entschlüsseln von Dateien, Nachrichten und Signaturen verfügbar sind.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Erforderliche Schlüssel Container, Schlüssel und Zertifikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d1f01a59c83ea21437608608e033a2ee0f8fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759463"
---
# <a name="necessary-key-containers-keys-and-certificates"></a><span data-ttu-id="e4664-103">Erforderliche Schlüssel Container, Schlüssel und Zertifikate</span><span class="sxs-lookup"><span data-stu-id="e4664-103">Necessary Key Containers, Keys, and Certificates</span></span>

<span data-ttu-id="e4664-104">Die Beispiel Programme in den folgenden Abschnitten führen Vorgänge aus, die erfordern, dass [*öffentliche/private Schlüsselpaare*](../secgloss/p-gly.md) zum Verschlüsseln und Entschlüsseln von Dateien, Nachrichten und Signaturen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e4664-104">Example programs in the following sections perform operations that require [*public/private key pairs*](../secgloss/p-gly.md) to be available for encrypting and decrypting files, messages, and signatures.</span></span> <span data-ttu-id="e4664-105">Viele dieser Programme werden zur Laufzeit kompiliert, verknüpft und ausgeführt, schlagen aber fehl, ohne dass in diesen speichern ordnungsgemäße [*Schlüssel Container*](../secgloss/k-gly.md), Schlüssel, [*Zertifikat Speicher*](../secgloss/c-gly.md)und Zertifikate vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e4664-105">Many of these programs will compile, link, and run but fail at run time without the existence of proper [*key containers*](../secgloss/k-gly.md), keys, [*certificate stores*](../secgloss/c-gly.md), and certificates in those stores.</span></span>

<span data-ttu-id="e4664-106">Außerdem müssen einige der Zertifikate im My-Speicher einige erweiterte Eigenschaften haben.</span><span class="sxs-lookup"><span data-stu-id="e4664-106">In addition, some of the certificates in the MY store must have some of their extended properties set.</span></span>

<span data-ttu-id="e4664-107">Der erforderliche Standardschlüssel Container kann erstellt werden, indem das Programm im [Beispiel C-Programm: Erstellen eines Schlüssel Containers und Erstellen von Schlüsseln](example-c-program-creating-a-key-container-and-generating-keys.md)ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4664-107">Creating the needed default key container can be done by running the program in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span> <span data-ttu-id="e4664-108">Beachten Sie, dass bei der Erstellung eines Schlüssel Containers nicht automatisch öffentliche/private Schlüsselpaare generiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4664-108">Note that the creation of a key container does not automatically generate public/private key pairs.</span></span> <span data-ttu-id="e4664-109">Das Beispielprogramm erstellt jedoch den Schlüssel Container und generiert die Paare aus öffentlichem und privatem Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="e4664-109">The example program, however, both creates the key container and generates the public/private key pairs.</span></span>

<span data-ttu-id="e4664-110">Nachdem öffentliche/private Schlüsselpaare generiert wurden, können Test Zertifikate, die diese Schlüssel verwenden, von einer [*Zertifizierungs*](../secgloss/c-gly.md) Stelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e4664-110">After public/private key pairs have been generated, test certificates using those keys can be obtained from a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="e4664-111">Einige der Programme gehen davon aus, dass Zertifikate mit bestimmten Antragsteller Namen im eigenen Systemspeicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e4664-111">Several of the programs assume that certificates with specific subject names exist in the MY system store.</span></span> <span data-ttu-id="e4664-112">Insbesondere suchen mehrere Programme nach Zertifikaten mit den Antragsteller Namen "Full Test CERT" und "Hortense".</span><span class="sxs-lookup"><span data-stu-id="e4664-112">In particular, several programs look for certificates with the subject names "Full Test Cert" and "Hortense."</span></span> <span data-ttu-id="e4664-113">Die Antragsteller Namen für die Zertifikate können im Code geändert werden, damit Sie mit den Antragsteller Namen von Zertifikaten identisch sind, die im My-Zertifikat Speicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e4664-113">The subject names for the certificates may be changed in the code to match the subject names of certificates that exist in the MY certificate store.</span></span>

<span data-ttu-id="e4664-114">Durch Ausführen des Beispiel Programms im [Beispiel C-Programm: durch das Auflisten der Zertifikate in einem Speicher](example-c-program-listing-the-certificates-in-a-store.md) werden alle Zertifikate in einem Speicher und alle erweiterten Eigenschaften angezeigt, die für diese Zertifikate festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e4664-114">Running the example program in [Example C Program: Listing the Certificates in a Store](example-c-program-listing-the-certificates-in-a-store.md) will display all of the certificates in a store and all of the extended properties that are set on those certificates.</span></span>

 

 
