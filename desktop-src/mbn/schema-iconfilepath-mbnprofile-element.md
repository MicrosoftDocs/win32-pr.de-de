---
description: Enthält den Pfad der Symbol Datei für die Verbindung.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Iconfilepath (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343698"
---
# <a name="iconfilepath-mbnprofile-element"></a><span data-ttu-id="f1372-103">Iconfilepath (mbnprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="f1372-103">ICONFilePath (MBNProfile) Element</span></span>

<span data-ttu-id="f1372-104">Das **iconfilepath (mbnprofile)** -Element enthält den Pfad der Symbol Datei für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f1372-104">The **ICONFilePath (MBNProfile)** element contains the path of the icon file for the connection.</span></span>

<span data-ttu-id="f1372-105">Die Benutzeroberfläche für die Betriebssystem Verbindung zeigt dieses Symbol an, wenn eine Verbindung mit diesem Element hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f1372-105">The operating system connection UI will display this icon when a connection is made using this element.</span></span>

<span data-ttu-id="f1372-106">Wenn Sie den XML-Code zum Erstellen des Profils in [**der Methode "**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) Methode" von " [**imbnconnectionprofilemanager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) " übergeben, sollte dieser Pfad auf den Quell Speicherort der Symbol Datei verweisen.</span><span class="sxs-lookup"><span data-stu-id="f1372-106">When passing the XML for creating the profile in the [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) method of the [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) interface, this path should point to the source location of the icon file.</span></span> <span data-ttu-id="f1372-107">Bei erfolgreicher Erstellung des [**imbnconnectionprofile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) -Objekts kopiert der Mobile Breitbanddienst die Symbol Datei im internen Speicher, und der Profilpfad wird geändert, um dies widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="f1372-107">On successful creation of [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) object, the Mobile Broadband service will copy the icon file in it's internal store and the profile path will be modified to reflect this.</span></span>

<span data-ttu-id="f1372-108">Die Symbol Datei sollte das BMP-Format mit einer Größe von 32 x 32 Pixel aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f1372-108">The icon file should be in .bmp format with 32X32 pixel dimension.</span></span>

<span data-ttu-id="f1372-109">Dieses Element ist eine Zeichenfolge mit einer Länge von bis zu 1024 Zeichen, die einen absoluten Dateipfad enthält.</span><span class="sxs-lookup"><span data-stu-id="f1372-109">This element is a string of length up to 1024 characters, containing an absolute file path.</span></span>

<span data-ttu-id="f1372-110">Das-Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="f1372-110">The element is optional.</span></span>

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

<span data-ttu-id="f1372-111">Das **iconfilepath** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="f1372-111">The **ICONFilePath** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1372-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1372-112">Requirements</span></span>



| <span data-ttu-id="f1372-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1372-113">Requirement</span></span> | <span data-ttu-id="f1372-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f1372-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f1372-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1372-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f1372-116">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f1372-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f1372-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1372-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f1372-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f1372-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="f1372-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1372-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1372-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="f1372-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f1372-121">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="f1372-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="f1372-122">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="f1372-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f1372-123">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="f1372-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




