---
description: Definiert ein paar von 802,11-Authentifizierungs-und Verschlüsselungsalgorithmen, die gleichzeitig auf der 802,11-Station aktiviert werden können.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: DOT11_AUTH_CIPHER_PAIR Struktur (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358541"
---
# <a name="dot11_auth_cipher_pair-structure"></a><span data-ttu-id="29b9b-103">DOT11 \_ auth- \_ Chiffre- \_ paar-Struktur</span><span class="sxs-lookup"><span data-stu-id="29b9b-103">DOT11\_AUTH\_CIPHER\_PAIR structure</span></span>

<span data-ttu-id="29b9b-104">Die **DOT11 \_ auth- \_ Chiffre- \_ paar** -Struktur definiert ein paar von 802,11-Authentifizierungs-und Verschlüsselungsalgorithmen, die gleichzeitig auf der 802,11-Station aktiviert werden können.</span><span class="sxs-lookup"><span data-stu-id="29b9b-104">The **DOT11\_AUTH\_CIPHER\_PAIR** structure defines a pair of 802.11 authentication and cipher algorithms that can be enabled at the same time on the 802.11 station.</span></span>

## <a name="syntax"></a><span data-ttu-id="29b9b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29b9b-105">Syntax</span></span>


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a><span data-ttu-id="29b9b-106">Member</span><span class="sxs-lookup"><span data-stu-id="29b9b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="29b9b-107">**Authalgoid**</span><span class="sxs-lookup"><span data-stu-id="29b9b-107">**AuthAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="29b9b-108">Ein Authentifizierungsalgorithmus, der einen enumerierten Typ des [**DOT11 \_ auth- \_ Algorithmus**](dot11-auth-algorithm.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="29b9b-108">An authentication algorithm that uses a [**DOT11\_AUTH\_ALGORITHM**](dot11-auth-algorithm.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="29b9b-109">**Cipheralgoid**</span><span class="sxs-lookup"><span data-stu-id="29b9b-109">**CipherAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="29b9b-110">Ein Verschlüsselungsalgorithmus, der einen enumerierten Typ des [**DOT11 \_ Chiffre \_ Algorithmus**](dot11-cipher-algorithm.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="29b9b-110">A cipher algorithm that uses a [**DOT11\_CIPHER\_ALGORITHM**](dot11-cipher-algorithm.md) enumerated type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29b9b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29b9b-111">Remarks</span></span>

<span data-ttu-id="29b9b-112">Die DOT11 \_ auth- \_ Chiffre \_ -paar-Struktur definiert einen Authentifizierungs-und Chiffre Algorithmus, der zusammen für Basic Service Set (BSS)-Netzwerkverbindungen aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="29b9b-112">The DOT11\_AUTH\_CIPHER\_PAIR structure defines an authentication and cipher algorithm that can be enabled together for basic service set (BSS) network connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="29b9b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29b9b-113">Requirements</span></span>



| <span data-ttu-id="29b9b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29b9b-114">Requirement</span></span> | <span data-ttu-id="29b9b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="29b9b-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29b9b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29b9b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="29b9b-117">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29b9b-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="29b9b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29b9b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="29b9b-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29b9b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="29b9b-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="29b9b-120">Redistributable</span></span><br/>          | <span data-ttu-id="29b9b-121">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="29b9b-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="29b9b-122">Header</span><span class="sxs-lookup"><span data-stu-id="29b9b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="29b9b-123"><dt>Wlantypes. h (Include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29b9b-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29b9b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29b9b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29b9b-125">**DOT11 \_ auth- \_ Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="29b9b-125">**DOT11\_AUTH\_ALGORITHM**</span></span>](dot11-auth-algorithm.md)
</dt> <dt>

[<span data-ttu-id="29b9b-126">**DOT11- \_ Chiffre \_ Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="29b9b-126">**DOT11\_CIPHER\_ALGORITHM**</span></span>](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




