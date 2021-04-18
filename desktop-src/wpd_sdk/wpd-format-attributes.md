---
description: 'Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für Formate auf einem Geräte Dienst. Diese Attribute werden von der iportabledeviceservicecapabili:: getformattribute-Methode zurückgegeben.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Format Attribute (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371152"
---
# <a name="format-attributes"></a><span data-ttu-id="85389-104">Format Attribute</span><span class="sxs-lookup"><span data-stu-id="85389-104">Format Attributes</span></span>

<span data-ttu-id="85389-105">Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für Formate auf einem Geräte Dienst.</span><span class="sxs-lookup"><span data-stu-id="85389-105">For Windows 7, Windows Portable Devices supports the following attributes for formats on a device service.</span></span> <span data-ttu-id="85389-106">Diese Attribute werden von der [**iportabledeviceservicecapabili:: getformattribute**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85389-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method.</span></span>




| <span data-ttu-id="85389-107">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="85389-107">**Attribute**</span></span>                        | <span data-ttu-id="85389-108">**VarType**</span><span class="sxs-lookup"><span data-stu-id="85389-108">**VarType**</span></span>    | <span data-ttu-id="85389-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85389-109">**Description**</span></span>                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85389-110">**WPD- \_ Format \_ Attribut \_ MimeType**</span><span class="sxs-lookup"><span data-stu-id="85389-110">**WPD\_FORMAT\_ATTRIBUTE\_MIMETYPE**</span></span> | <span data-ttu-id="85389-111">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="85389-111">**VT\_LPWSTR**</span></span> | <span data-ttu-id="85389-112">Der MIME-Typ des Formats.</span><span class="sxs-lookup"><span data-stu-id="85389-112">The format MIME type.</span></span>                                                                                                     |
| <span data-ttu-id="85389-113">**\_ \_ Attribut \_ Name für WPD-Format**</span><span class="sxs-lookup"><span data-stu-id="85389-113">**WPD\_FORMAT\_ATTRIBUTE\_NAME**</span></span>     | <span data-ttu-id="85389-114">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="85389-114">**VT\_LPWSTR**</span></span> | <span data-ttu-id="85389-115">Eine Zeichenfolge, die den Skript freundlichen Namen des Formats angibt.</span><span class="sxs-lookup"><span data-stu-id="85389-115">A string that specifies the script-friendly name of the format.</span></span> <span data-ttu-id="85389-116">Gültige Zeichen sind alphanumerisch \[ a-Za-z0-9 \] und ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="85389-116">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="85389-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85389-117">Requirements</span></span>



| <span data-ttu-id="85389-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85389-118">Requirement</span></span> | <span data-ttu-id="85389-119">Wert</span><span class="sxs-lookup"><span data-stu-id="85389-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="85389-120">Header</span><span class="sxs-lookup"><span data-stu-id="85389-120">Header</span></span><br/> | <dl> <span data-ttu-id="85389-121"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="85389-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85389-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85389-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85389-123">**Eigenschaften und Attribute**</span><span class="sxs-lookup"><span data-stu-id="85389-123">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




