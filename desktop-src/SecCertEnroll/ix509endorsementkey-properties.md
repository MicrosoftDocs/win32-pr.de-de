---
description: Die IX509EndorsementKey-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: IX509EndorsementKey-Eigenschaften
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362319"
---
# <a name="ix509endorsementkey-properties"></a>IX509EndorsementKey-Eigenschaften

Die [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Längeneigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | Die Bitlänge des Endorsement Key. Sie können nur auf diese Eigenschaft zugreifen, nachdem die [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) -Methode aufgerufen wurde.<br/>                                                                                                                                                                                            |
| [**Geöffnete Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Gibt an, ob die [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) -Methode erfolgreich aufgerufen wurde.<br/>                                                                                                                                                                                                                                            |
| [**ProviderName-Eigenschaft**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | Der Name des Verschlüsselungsanbieters. Der Standardwert ist der Kryptografieanbieter der Microsoft-Plattform. Sie müssen die [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) -Eigenschaft festlegen, bevor Sie die [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) -Methode aufzurufen. Sie können die **providerName** -Eigenschaft nicht ändern, nachdem Sie die **Open** -Methode aufgerufen haben.<br/> |



 

 

 




