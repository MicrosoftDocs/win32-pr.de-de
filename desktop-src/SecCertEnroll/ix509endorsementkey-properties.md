---
description: Die IX509EndorsementKey-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: IX509EndorsementKey-Eigenschaften
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41d135205680e4c998c1157844cfa66a9ef9bd7ef4df5ff8258a31e562a685e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117776188"
---
# <a name="ix509endorsementkey-properties"></a>IX509EndorsementKey-Eigenschaften

Die [**IX509EndorsementKey-Schnittstelle**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) macht die folgenden Eigenschaften verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Längeneigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | Die Bitlänge des Endorsement Key. Sie können erst auf diese Eigenschaft zugreifen, nachdem die [**Open-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) aufgerufen wurde.<br/>                                                                                                                                                                                            |
| [**Geöffnete Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Gibt an, ob die [**Open-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) erfolgreich aufgerufen wurde.<br/>                                                                                                                                                                                                                                            |
| [**ProviderName-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | Der Name des Verschlüsselungsanbieters. Der Standardwert ist der Microsoft Platform Crypto Provider. Sie müssen die [**ProviderName-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) festlegen, bevor Sie die [**Open-Methode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) aufrufen. Sie können die **ProviderName-Eigenschaft** nicht mehr ändern, nachdem Sie die **Open-Methode** aufgerufen haben.<br/> |



 

 

 




